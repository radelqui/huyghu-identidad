# Plan futuro — Disclaimer corporativo automático server-side
Fecha: 2026-05-12
Tenant: huyghusrl.onmicrosoft.com (Microsoft 365)

═══════════════════════════════════════════════════════════
## PROBLEMA OBSERVADO HOY
═══════════════════════════════════════════════════════════

Al instalar la firma manualmente en Outlook Web para `carlos@huyghusrl.com`:

1. **El logo SVG embebido como `data:image/svg+xml;base64`** se ve correctamente EN el editor de Outlook, pero algunos clientes de correo (Outlook 2016, Gmail) pueden:
   - Convertirlo a archivo adjunto separado
   - No renderizarlo si bloquean imágenes externas
   - Romper el layout en modo dark de algunos clientes

2. **La firma es per-usuario**: cada empleado tendría que configurar la suya manualmente — 8 personas × 5 minutos = 40 min, con riesgo de errores

3. **Si Carlos cambia el logo o disclaimer**: hay que reconfigurar las 8 firmas una por una

═══════════════════════════════════════════════════════════
## SOLUCIÓN PROPUESTA — 3 capas
═══════════════════════════════════════════════════════════

### CAPA 1 — Logo en CDN público (URL absoluta, no data URI)

**Acción**:
- Subir el SVG del logo HUYGHU a una URL pública estable
- Opciones de hosting:
  - **A** `https://app.huyghusrl.com/assets/logo-firma-huyghu.svg` (GitHub Pages, gratis, ya tenemos)
  - **B** `https://assets.huyghusrl.com/logo.svg` (subdominio nuevo en Cloudflare, mejor branding)
  - **C** Subir al SharePoint con URL pública (más control de acceso)

**Recomendación**: opción A inmediata (subir a `radelqui/huyghu-identidad` en `/assets/logo-firma-huyghu.svg`)

**Beneficio**:
- El cliente de correo solo guarda la URL, no la imagen → no convierte a adjunto
- Si Carlos quiere cambiar el logo, edita el archivo en GitHub y se propaga a TODOS los emails ya enviados (porque cargan desde la misma URL)
- Tamaño del HTML de firma cae de ~4 KB (con SVG embebido) a ~1 KB

---

### CAPA 2 — Disclaimer automático via Exchange Transport Rule

**Acción** (la hace Carlos como admin del tenant):

1. Entrar a **Exchange Admin Center**: `https://admin.exchange.microsoft.com/`
2. Ir a **Flujo de correo → Reglas**
3. Crear **nueva regla**: "Añadir disclaimer corporativo"
4. Condición: "Aplicar a todos los mensajes" (o filtrar por dominio remitente `*@huyghusrl.com`)
5. Acción: "**Aplicar exención de cumplimiento de mensajes → Aplicar declaración**"
6. Pegar el HTML del disclaimer:

```html
<table cellpadding="0" cellspacing="0" border="0" style="border-collapse:collapse;margin-top:14px;border-top:1px solid #E5E5E5;padding-top:10px;font-family:Arial,Helvetica,sans-serif;font-size:9px;color:#666666;line-height:1.55;max-width:600px;">
  <tr><td>
    <strong style="color:#8B5E1A;letter-spacing:.5px;">⚠ AVISO DE CONFIDENCIALIDAD</strong> — Este mensaje y sus anexos son <strong>estrictamente confidenciales</strong>, contienen información protegida y están destinados al uso exclusivo del destinatario. Si usted ha recibido este correo por error, le rogamos que lo <strong>notifique inmediatamente al remitente</strong>, lo <strong>devuelva a su origen sin reenviarlo</strong> y proceda a <strong>eliminarlo de todos sus dispositivos</strong>. Está prohibido cualquier uso, divulgación, copia, distribución o reenvío no autorizado de este contenido. Esta comunicación está amparada bajo la <strong>Ley 172-13 sobre Protección de Datos Personales</strong> de la República Dominicana, el <strong>secreto profesional</strong> de los Contadores Públicos y las normas internas del Grupo Chrytsa. RNC HUYGHU & Asociados, S.R.L.: 131-047939 · ICPARD ⏵ miembros activos.
  </td></tr>
</table>
```

7. Opciones avanzadas:
   - **Fallback**: si el disclaimer no se puede insertar (mensaje cifrado, etc.), envíalo igualmente (no bloquear)
   - **Modo**: Aplicar (no Test/Audit)

**Beneficio**:
- TODOS los empleados del tenant tienen disclaimer automático sin configurar nada
- Si Carlos cambia el texto legal, basta editar la regla una vez
- Los empleados solo configuran la firma personal (nombre, cargo, teléfono) — el disclaimer es server-side
- Cumple Ley 172-13 sin depender de la disciplina del empleado

**Costo**: Incluido en cualquier plan Microsoft 365 Business Standard o superior

---

### CAPA 3 — Cloud Signatures (firma centralizada por usuario)

**Estado**: Microsoft lanzó **Outlook Cloud Signatures** (también llamado "Roaming Signatures") en 2023. Permite que cada usuario tenga su firma sincronizada en todos sus dispositivos (Web, Desktop, Mobile).

**Acción para Carlos** (admin):

1. Ir a **Microsoft 365 admin center → Configuración → Servicios → Configuración de firma de Outlook**
2. Habilitar "Firmas en la nube"
3. Crear un **template maestro** con campos dinámicos:
   - `{firstName}` `{lastName}` — del Active Directory
   - `{jobTitle}` — del AD
   - `{phone}` — del AD
   - `{email}` — automático
   - Logo: URL absoluta (capa 1)
   - Disclaimer: NO necesario aquí, ya viene de capa 2

4. Aplicar la template a un grupo de seguridad (ej. "HUYGHU - Personal").

**Beneficio**:
- Cuando Carlos contrate un nuevo empleado y lo añada al AD, automáticamente tendrá firma corporativa al primer correo
- Los datos personales vienen del AD → si cambias el cargo de un empleado en AD, su firma se actualiza sola
- Funciona en Outlook Mobile (no solo Web)

**Alternativa más simple** (sin Cloud Signatures): usar la **MISMA Transport Rule (Capa 2)** para inyectar también la firma personal con datos del remitente vía variables `%%Sender_FirstName%%`, `%%Sender_LastName%%`, etc.

---

═══════════════════════════════════════════════════════════
## ROADMAP DE IMPLEMENTACIÓN
═══════════════════════════════════════════════════════════

### FASE 1 — Hoy (manual, prueba) ✅ HECHO
- Firma de Carlos personalizada con tabla simple, disclaimer embebido
- Sirve para que Carlos pueda mandarle a Cristian el correo profesional YA

### FASE 2 — Esta semana (cuando Carlos tenga 30 min)
1. Subir logo SVG a `radelqui/huyghu-identidad/assets/logo-firma-huyghu.svg`
2. URL pública: `https://app.huyghusrl.com/huyghu-identidad/assets/logo-firma-huyghu.svg`
3. Actualizar las 12 firmas del bundle para usar la URL en vez de data URI
4. Actualizar la firma activa de Carlos en Outlook Web (cambiar el `<img src="data:...">` por `<img src="https://...">`)

### FASE 3 — Cuando Carlos tenga acceso al Exchange Admin Center
1. Crear Transport Rule "Disclaimer Corporativo" con el HTML de la capa 2
2. Aplicarla a todo `*@huyghusrl.com`
3. Hacer prueba con un correo de prueba a una cuenta externa (gmail.com) y verificar que el disclaimer aparece al final
4. **REMOVER el disclaimer manual de la firma personal** de cada empleado (porque ahora viene del servidor)

### FASE 4 — Onboarding masivo
1. Crear template Cloud Signature para el grupo "HUYGHU - Personal"
2. Documentar proceso en `EMPLOYEE-ONBOARDING.md` (cuando se contrate alguien)
3. Migrar los 8 empleados existentes (Carlos, Cristian, Yolanda, Diego, Jrivera, Griselda, Joel, Dany Garcia)

═══════════════════════════════════════════════════════════
## DECISIONES PENDIENTES — CARLOS
═══════════════════════════════════════════════════════════

1. ¿Subimos el logo a `app.huyghusrl.com` (GitHub Pages) o creamos subdominio nuevo `assets.huyghusrl.com`?
2. ¿Carlos tiene acceso de admin global al tenant `huyghusrl.onmicrosoft.com`? Si no, ¿quién lo tiene?
3. ¿Aplicamos Transport Rule a TODO el tenant, o solo al grupo HUYGHU (excluyendo Chrytsa si tiene otro dominio)?
4. ¿El nombre del **Socio Director** que debe aparecer en las firmas oficiales es Cristian Huyghu? (lo confirmó en cuenta `cristian@huyghusrl.com` que aparece en la lista de empleados)

═══════════════════════════════════════════════════════════
## REFERENCIAS TÉCNICAS
═══════════════════════════════════════════════════════════

- Exchange Transport Rules — disclaimer: https://learn.microsoft.com/exchange/security-and-compliance/mail-flow-rules/disclaimers-signatures-footers-or-headers
- Outlook Roaming Signatures: https://learn.microsoft.com/outlook/troubleshoot/signatures/cloud-signature
- HTML Email best practices (table-based): https://www.litmus.com/blog/the-ultimate-guide-to-html-email-design
- Test de compatibilidad: https://litmus.com/ o https://www.emailonacid.com/
