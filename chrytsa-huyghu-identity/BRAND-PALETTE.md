# Brand Palette · v2.0.2 — Chrytsa & HUYGHU

Paleta institucional actualizada (mayo 2026). Reemplaza la paleta oro/negro v1.0.

---

## Colores Primarios

| Token | HEX | RGB | CMYK | Pantone aprox. | Uso |
|-------|-----|-----|------|----------------|-----|
| **Azul Corporativo** | `#2B6CB0` | 43 · 108 · 176 | 76 · 39 · 0 · 31 | 285 C | Contorno esfera, tagline "CONTADORES PÚBLICOS", elementos estructurales, divisores |
| **Verde Lima** | `#8DC63F` | 141 · 198 · 63 | 29 · 0 · 68 · 22 | 369 C | Wordmark "Huyghu & Asoc. SRL", bandas internas de la esfera, CTAs, highlights |
| **Blanco Papel** | `#FFFFFF` | 255 · 255 · 255 | 0 · 0 · 0 · 0 | — | Fondo principal canónico |
| **Gris Oscuro** | `#1A1A2E` | 26 · 26 · 46 | 43 · 43 · 0 · 82 | Black 7 C | Body text, fondos premium oscuros |

---

## Gradiente Azul Oficial

```css
linear-gradient(135deg,
  #5B9BD5 0%,    /* azul claro */
  #2B6CB0 35%,   /* azul corporativo */
  #1E5090 70%,   /* azul medio */
  #163B6B 100%   /* azul profundo */
);
```

| Stop | HEX | Uso |
|------|-----|-----|
| 0% | `#5B9BD5` | Highlight, hover digital |
| 35% | `#2B6CB0` | Base canónica del gradiente |
| 70% | `#1E5090` | Mid-tone, profundidad |
| 100% | `#163B6B` | Sombra final, texto meta sobre claro |

---

## Colores Secundarios

| Token | HEX | Uso |
|-------|-----|-----|
| Azul claro | `#5B9BD5` | Headlines premium, highlights |
| Azul medio | `#1E5090` | Hover sobre primary, mid-tones |
| Azul profundo | `#163B6B` | Sombras, eyebrows en claro |
| Lima oscuro | `#6BA32E` | Hover sobre verde lima |
| Lima claro | `#B8E07A` | Acento sutil, badges secundarios |
| Gris frío 1 | `#9CA8B8` | Body secundario sobre oscuro |
| Gris frío 2 | `#6B7A8C` | Footer, micro-text |
| Gris frío 3 | `#3F4858` | Captions premium |
| Línea sutil | `rgba(43,108,176,.18)` | Bordes, separadores |
| Card claro | `#F4F8FB` | Surface cards en light theme |
| App bg frío | `#E8EEF5` | Fondo neutro de la app |

---

## Funcionales

| Token | HEX | Uso |
|-------|-----|-----|
| Success | `#1F8A5B` | Confirmaciones DGII, pagos OK *(armoniza con verde lima)* |
| Warning | `#D97757` | Recordatorios de vencimiento |
| Error | `#B83A26` | Errores críticos (uso limitado) |

---

## Reglas de Uso

1. **Lima `#8DC63F` es exclusivo del wordmark y CTAs**. No usar en body text largo (cansa la vista).
2. **Azul `#2B6CB0` es el color estructural**: contornos, taglines, divisores, eyebrows. No mezclar con otros azules.
3. **Fondo canónico = `#FFFFFF`** (blanco puro). Para variantes premium oscuras usar `#1A1A2E` (gris oscuro azulado), nunca negro puro.
4. **Contraste mínimo AA**: lima sobre blanco = 2.5:1 ⚠ (usar SOLO para wordmark/CTAs grandes 18pt+) · azul sobre blanco = 5.2:1 ✓ · gris oscuro sobre blanco = 14.8:1 ✓
5. **Para impresión foil**: Pantone 285 C (azul) + Pantone 369 C (lima). Para Touche Cover 350g + UV selectivo sobre lima.
6. **No combinar lima con amarillos, naranjas o dorados**. La paleta es bicolor: azul + lima sobre blanco.

---

## Logo · Aplicación de color

### HUYGHU & Asociados
- **Contorno esfera**: `#2B6CB0` (azul corporativo)
- **3 bandas diagonales internas**: `#8DC63F` (verde lima)
- **Wordmark "Huyghu & Asoc. SRL"**: `#8DC63F` (verde lima)
- **Tagline "CONTADORES PÚBLICOS"**: `#2B6CB0` (azul corporativo)

### Grupo Chrytsa (matriz)
- **Anillo orbital exterior** *(distintivo de holding)*: `#2B6CB0` (azul corporativo)
- **Contorno esfera interior**: `#2B6CB0` (azul corporativo)
- **3 bandas diagonales internas**: `#8DC63F` (verde lima)
- **Wordmark "Grupo Chrytsa"**: `#8DC63F` (verde lima)
- **Tagline "ASESORES"**: `#2B6CB0` (azul corporativo)

El anillo orbital exterior es la única diferencia visual entre Chrytsa y HUYGHU: comunica "matriz que encierra/contiene a las filiales".

---

## Tipografía aparejada

- Headlines display → **Cinzel** (Google Fonts) · serif inscripcional
- Body & UI → **Inter** (Google Fonts) · sans-serif neutro
- Tracking labels → **Montserrat** (Google Fonts) · sans-serif geométrico
- Code / meta → **JetBrains Mono** (Google Fonts) · monospace técnico
- *Alternativa script para wordmark*: **Allura** o **Great Vibes** (Google Fonts) para reproducir el estilo caligráfico del bordado original

---

**v2.0.2** · Paleta oficial vigente · Símbolo corregido a círculo cerrado · Sustituye a v1.0 (oro/negro) · Mayo 2026
