# Chrytsa & HUYGHU — Identidad Visual v2.0.2

Sistema de identidad corporativa para **Grupo Chrytsa** (matriz · holding) y **HUYGHU & Asociados, SRL** (filial contable), República Dominicana.

Entrega completa en 8 bloques. Material editable en herramientas estándar (Figma, Illustrator, Inkscape, PowerPoint, Word). Sin dependencias propietarias.

---

## ⚠ v2.0.3 — Logo definitivo propagado (mayo 2026)

El símbolo definitivo (extraído del bordado/PDF originales) es una **esfera azul** con una **S serpentina lima** de 3 segmentos. **HUYGHU** añade un **arco exterior fino** que abraza la esfera; **Grupo Chrytsa** usa la esfera limpia **sin arco** (ya no lleva anillo orbital punteado). Geometría + colores propagados a los 8 bloques: guías, deck, tarjetas, firmas, emails, favicons (PNG + SVG regenerados) y 36 piezas sociales (SVG + PNG). Fuente única de verdad en `logo/` (`huyghu-mark.svg`, `chrytsa-mark.svg`, `*-lockup.svg`).
Nota: los `favicon.ico` binarios multi-tamaño no se regeneraron (formato ICO); reexportar desde `favicon-48.png` si se requiere.

Colores oficiales: **Azul** `#1B3A6B` · **Verde lima** `#99FF00`.

## ⚠ v2.0 — Cambio de paleta (mayo 2026)

Esta versión sustituye a v1.0 (oro/negro). La nueva identidad oficial vuelve a los **colores originales del bordado HUYGHU**:

- **Azul Corporativo** `#1B3A6B` — color estructural (esfera, arco, taglines, divisores)
- **Verde Lima** `#99FF00` — acento de marca (wordmark, S serpentina, CTAs)
- **Blanco** `#FFFFFF` — fondo principal canónico
- **Gris Oscuro** `#1A1A2E` — body text, fondos premium oscuros

Ver `BRAND-PALETTE.md` para la paleta completa con HEX/RGB/CMYK/Pantone.

### Logo de Chrytsa (derivado del de HUYGHU)

Ambas marcas comparten la **esfera azul con la S serpentina lima** como base. La única diferencia es que **HUYGHU lleva un arco exterior fino** que abraza la esfera, mientras que **Grupo Chrytsa usa la esfera limpia sin arco**. El logo de Chrytsa **no usa corona, "G" coronada ni anillo orbital punteado** (legacy descartado).

---

## Índice de carpetas

| Bloque | Carpeta | Contenido | Formato |
|--------|---------|-----------|---------|
| 01 | `guidelines/Logo System.html` | 12 variantes de logo (6 Chrytsa + 6 HUYGHU) + grillas construcción 12×12 | HTML + SVG inline |
| 02 | `favicons/` | 20 archivos favicon (10 por marca) + `manifest.json` PWA + `Favicon Preview.html` | ICO · PNG · SVG · JSON |
| 03 | `guidelines/Email Signatures.html` | 12 firmas (3 estilos × 2 themes × 2 marcas) table-based | HTML inline-CSS |
| 04 | `cards/` + `guidelines/Business Cards.html` | Tarjetas impresas 85×55mm + vCard digital 1080×1920 con QR | HTML imprimible + SVG |
| 05 | `deck/HUYGHU-Pitch-Deck-v1.0.pptx` + `guidelines/Pitch Deck.html` | Pitch deck institucional 15 slides editable | PPTX + HTML |
| 06 | `guidelines/Brand Guidelines.html` | Manual de marca 22 páginas A4 imprimible | HTML → PDF |
| 07 | `emails/` | 6 plantillas transaccionales + `Email Templates.html` gallery | HTML table-based |
| 08 | `social/` | 12 templates RRSS × 3 dimensiones · 36 SVG + 36 PNG + `Social Templates.html` | SVG + PNG |

---

## Cómo navegar

1. **Empieza por** `guidelines/Logo System.html` — el canvas oficial con las 12 variantes del nuevo logo.
2. **Manual oficial**: `guidelines/Brand Guidelines.html` — 22 páginas A4. Cmd+P → PDF.
3. **Para crear piezas nuevas**: parte de las plantillas en `social/`, `emails/`, `deck/`, `cards/`.
4. **Paleta canónica**: `BRAND-PALETTE.md` (raíz).

---

## Placeholders que faltan completar

Los únicos campos que Carlos debe llenar manualmente antes de imprimir o enviar:

- `[Nombre del Socio Director]` → nombre real del socio (Carlos De La Torre u otro firmante)
- `[+1 809-XXX-XXXX]` → teléfono oficina real
- `[RNC: XXX-XXXXX-X]` → RNC oficial HUYGHU y Chrytsa
- `[Cliente Ejemplo XX]` en casos de éxito → 3 nombres de clientes reales (con permiso)
- `[ICPARD #XXXX]` → número de colegiación profesional
- `[Filial 03]` y `[Filial 04]` → las 2 empresas del Grupo Chrytsa aún sin nombre
- `info@huyghu.com` / `www.huyghu.com` → confirmar dominio definitivo (huyghu.com vs huyghusrl.com)

---

## Convenciones técnicas

- Los HTML se abren en cualquier navegador moderno sin servidor local
- PPTX abre en PowerPoint 2016+, Keynote, Google Slides
- SVG editables con objetos nombrados (`bg`, `headline`, `body`, `cta`, `logo`)
- Tipografías Google Fonts gratuitas (Cinzel, Inter, Montserrat, JetBrains Mono)
- Colores críticos: **`#2B6CB0`** (azul) + **`#8DC63F`** (lima) + **`#FFFFFF`** (blanco)

---

## Changelog

- **v2.0.2** (mayo 2026) — **Corrección crítica del símbolo.** El logo real del bordado es un **círculo azul cerrado completo** atravesado por 3 bandas verde lima diagonales (−48°); no tiene arco abierto ni cola decorativa. SVG reescrito en los 8 bloques (Logo System, Favicons, Email Signatures, Business Cards, Pitch Deck, Brand Guidelines, Emails, Social). 36 SVGs sociales + 2 favicons + 7 HTML + 6 emails con data URI — todos propagados. Chrytsa conserva el anillo orbital exterior punteado como distintivo de matriz.
- **v2.0.1** (mayo 2026) — Reescritura del SVG del logo desde el bordado original (geometría con arco + cola — *corregida en v2.0.2*). Wordmark Huyghu en script Allura sobre Montserrat tracked. Aplicado a los 8 bloques. Símbolos legacy "G coronada" eliminados.
- **v2.0** (mayo 2026) — Cambio total de paleta a azul/lima sobre blanco. Logo Chrytsa rediseñado como derivación de la esfera HUYGHU + anillo orbital. Wordmark, taglines y todos los assets actualizados.
- **v1.0** (mayo 2026) — Entrega inicial con paleta oro/negro. *Obsoleta*.

---

## Contacto

Brand Manager · **Carlos De La Torre**  
HUYGHU & Asociados · Contadores Públicos  
Grupo Chrytsa · Puerto Plata, República Dominicana

---

**v2.0.2** · Entrega final corregida · Mayo 2026
