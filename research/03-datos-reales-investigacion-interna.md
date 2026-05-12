# Investigación interna profunda — HUYGHU & Chrytsa
Fecha: 2026-05-11
Fuentes: knowledge-hub KB · sypnose-memory (Memory Palace) · sypnose_kg (Knowledge Graph) · wiki HUYGHU servidor 217

═══════════════════════════════════════════════════════════
## DATOS OFICIALES CONFIRMADOS (alta confianza)
═══════════════════════════════════════════════════════════

### HUYGHU & Asociados, S.R.L.
| Campo | Valor | Fuente |
|---|---|---|
| Razón social oficial | **HUYGHU & ASOCIADOS, SRL** | Wiki `~/wiki/clientes/131047939-*.md` frontmatter |
| RNC | **131-047939** (sin guiones: `131047939`) | BD `clientes`, factura ID 11458, KB 8217 |
| Tipo | Despacho contable dominicano | Wiki SCHEMA.md |
| UUID empresa (sistema interno) | `616b8f1b-d3f1-403d-883b-aec3302363e5` | BD `empresas`, KB 8800 |
| Header dashboard | "Huyghu SRL" | KB 7253, 7928 |
| Clientes activos | **315** (confirmado wiki + BD) | Wiki index.md, KB 7026 |
| Contadores asignados | **14** | KB 9275 (migration 011 RLS) |
| Teléfono oficina | **809-261-7938** | Wiki ficha cliente 131047939 |
| Email administrativo | `agenda@huyghusrl.com` | KB 11523 (login real SaaS) |
| Email supervisor | `super@huyghusrl.com` | KB 11546 |
| Eslogan | "Su cumplimiento, nuestra prioridad" | Claude.ai memoria |

### Grupo Chrytsa
| Campo | Valor | Fuente |
|---|---|---|
| Dominio confirmado | **chrytsa.com** | BD `usuarios_sistema` (carlos@chrytsa.com) |
| Email Carlos | **carlos@chrytsa.com** | KB 7253 diagnóstico fix-supervisor-ov-310326 |
| Rol | Holding / Matriz | Claude.ai memoria |
| Empresas confirmadas | HUYGHU & Asociados + HUSPEC Consultores Legales | Claude.ai memoria |
| Empresas totales declaradas | 4 (2 sin nombrar) | Claude.ai memoria |

### Infraestructura digital HUYGHU (Microsoft 365 + Cloudflare)
| Recurso | URL/ID | Fuente |
|---|---|---|
| Tenant M365 (Azure AD) | `64052184-79f6-430c-a177-ce26497c225d` | wiki/fuentes/sharepoint-huyghu.md |
| SharePoint site | `https://huyghusrl.sharepoint.com/sites/HuyghuAsoc/` | Memory id 7766 |
| SharePoint user-drive | `https://huyghusrl-my.sharepoint.com/:x:/p/carlos/...` | Memory id 10711 |
| Subdominio O365 | `huyghusrl.onmicrosoft.com` (inferido) | URL my.sharepoint |
| Drive ID principal | `b!iT8BOI0tVk63zMchL2sqbM5oUA6ev5pFpKtPacwkDXctwe8rFsqdQIjnnnByLI2u` | Memory id 7766 |
| Azure App SP | `client_id=3665f3a2-e277-41e4-8d0e-0b64fd7082e3` | wiki SP |
| Azure App InboxIA | `client_id=3daea923-512e-460c-9e52-57340efd8a5d` | KB 16784 |
| Subdominio OCR | `ocr.huyghusrl.com` (FacturaIA prod) | KB 6445 |
| Empleados con email O365 | `carlos@huyghusrl.com`, `jrivera@huyghusrl.com`, `griselda@huyghusrl.com`, `joel@huyghusrl.com` (inferidos por SharePoint + cartas) | Memory ids 10711, 10708 |

═══════════════════════════════════════════════════════════
## EQUIPO HUYGHU (parcialmente confirmado)
═══════════════════════════════════════════════════════════

### Nombres confirmados (no acceso directo a BD, pero aparecen en memoria/KB)
1. **Carlos De La Torre** — Socio (PIN CRM 1234, dueño Chrytsa, email `carlos@chrytsa.com` + `carlos@huyghusrl.com`)
2. **Yolanda** — Equipo supervisor (memoria id 10826)
3. **Diego** — Equipo supervisor (memoria id 10826 — pendiente email cuando se cree)
4. **J. Rivera (jrivera)** — Equipo (aparece en SharePoint user-drive)
5. **Griselda** — Empleada (memoria — emails que parsea InboxIA)
6. **Joel** — Empleado (memoria — emails Griselda/Joel mencionados juntos)
7. **Cristian** — empleado/cliente (password genérica "CRISTIAN14" en spreadsheet master)

═══════════════════════════════════════════════════════════
## ASSETS DIGITALES PREVIOS HUYGHU
═══════════════════════════════════════════════════════════

### Sistemas operativos en producción
- **SaaS GestoriaRD** (`gestoriard.com` + `gestoriard.sypnose.cloud`): plataforma multi-tenant Next.js 15. HUYGHU es el primer y único tenant activo.
- **FacturaIA OCR**: app Android + API `ocr.huyghusrl.com` (HTTPS TLS verificado)
- **DGII Scraper**: pipeline 24/7 que extrae datos de portal DGII para los 315 clientes
- **Wiki HUYGHU**: `/home/gestoria/wiki/` con 329 archivos markdown, indexado en RAG
- **Inbox IA**: parser de correos cuenta `jrivera@huyghusrl.com` (más Carlos + Griselda + Joel)

### Sistema visual histórico (a DESCARTAR en el rebrand)
- Logo viejo: esfera azul/turquesa con arco envolvente + wordmark verde "Huyghu & Asoc. S.R.L."
- Paleta histórica:
  - Verde principal `#5CB85C`
  - Azul turquesa `#5BC0DE`
  - Gris oscuro `#333333`
  - Gris claro `#666666`
- Tipografía histórica: Arial (toda la familia)
- Dossier corporativo Word/PDF (octubre 2025) creado con Claude.ai
- Propuesta de Iguala Mensual formato EY (creada con Claude.ai)
- Plantilla maestra documentos con identidad visual

### Sistema visual NUEVO (a APLICAR en este brand kit)
- Logos confirmados por Carlos (4 PNG WhatsApp 2026-05-11): oro+negro, serif Trajan/Cinzel, símbolos G coronada (Chrytsa) + esfera fragmentada (HUYGHU)
- Paleta canónica: gold `#D4AF37` + ink `#0A0A0A` + gradient `#F4D773→#8B5E1A`
- Tipografía: Cinzel (wordmark) + Montserrat Medium (tagline) + Inter (body)

═══════════════════════════════════════════════════════════
## DATOS PENDIENTES (Carlos debe suministrar)
═══════════════════════════════════════════════════════════

1. ⏳ Fecha de fundación HUYGHU (la memoria dice "[Año]" placeholder)
2. ⏳ Fecha de fundación Grupo Chrytsa
3. ⏳ Nombre LEGAL del Socio Director (Carlos es socio pero ¿hay socios adicionales?)
4. ⏳ Nombres oficiales de las 4 empresas del Grupo Chrytsa (solo confirmadas HUYGHU + HUSPEC)
5. ⏳ RNC Grupo Chrytsa
6. ⏳ RNC HUSPEC Consultores Legales
7. ⏳ Teléfono comercial principal (la oficina tiene 809-261-7938)
8. ⏳ Número de matrícula ICPARD (Instituto Contadores Públicos Autorizados RD)
9. ⏳ Cuenta corporativa LinkedIn / Instagram (handles oficiales)

═══════════════════════════════════════════════════════════
## ACCIONES TOMADAS EN EL BRAND KIT
═══════════════════════════════════════════════════════════

El brand kit en construcción en Claude Design (project `019e19ce-d3af-7b58-95a9-631f9fa25b5f`) usa:

- **RNC HUYGHU**: `131-047939` (real, confirmado, NO placeholder)
- **Teléfono**: `+1 809-261-7938` (real, NO `[+1 809-XXX-XXXX]`)
- **Dominio**: `huyghu.com` + subdominios reales (`ocr.huyghusrl.com`, `gestoriard.com`)
- **Email general**: `info@huyghu.com` (genérico, Carlos confirma o cambia)
- **Email Brand Manager**: `marca@grupochrytsa.com` (sugerido, Carlos crea o cambia)
- **Dirección**: Torre Acrópolis, Piso 14, Av. Winston Churchill 93, Santo Domingo (de memoria Claude.ai)
- **Slogan**: "Su cumplimiento, nuestra prioridad"

Los datos NO confirmados (fecha fundación, nombre socio individual, etc.) quedan como placeholders `[entre corchetes]` con instrucciones claras de dónde editarlos en cada deliverable.

═══════════════════════════════════════════════════════════
## NOTA SOBRE LA RAZÓN SOCIAL: SRL vs S.R.L.
═══════════════════════════════════════════════════════════

- **Wiki frontmatter dice**: `HUYGHU & ASOCIADOS, SRL` (sin puntos)
- **Memoria Claude.ai dice**: `HUYGHU & Asociados, S.R.L.` (con puntos)
- **Logo PNG enviado por Carlos dice**: `HUYGHU & ASOCIADOS` (sin sufijo SRL en el wordmark — solo "CONTADORES PÚBLICOS")
- **Decisión brand**: usar `HUYGHU & ASOCIADOS · CONTADORES PÚBLICOS` en logo/wordmark (estilo elegante sin sufijo legal). Sufijo legal `S.R.L.` solo en documentos formales (recibos, facturas, contratos) — al pie en Inter 7pt.
