# Extracción de identidad — análisis visual de los 4 logos
Fecha: 2026-05-11
Fuente: 4 PNGs en `C:\Users\carlo\Downloads\logos\WhatsApp Image 2026-05-11 at 9.18.14-15 PM*.jpeg`

---

## Sistema visual compartido (Grupo Chrytsa + HUYGHU)

Ambas marcas comparten un **ADN visual común** (sub-marca dentro del grupo):
- Composición: marca circular (ícono superior + wordmark + underline gold + tagline tracking wide)
- Paleta: oro + negro + blanco
- Wordmark: serif clásico mayúsculas
- Tagline: sans-serif geometric tracking amplio
- Línea divisoria: oro sólido entre wordmark y tagline

Cada marca tiene su variante **fondo blanco** y **fondo negro** (las 4 imágenes adjuntas son los 4 cuadrantes de esta matriz).

---

## Paleta canónica extraída

### Oros (gradiente metálico)
| Token | HEX | Uso | Notas |
|---|---|---|---|
| `gold/highlight` | `#F4D773` | Highlight superior del gradiente, brillo del ícono | Tono champagne |
| `gold/primary` | `#D4AF37` | Oro principal "rich gold" — color base del wordmark sobre negro | Pantone Metallic 871 C aprox |
| `gold/mid` | `#B8862B` | Mid-tone del gradiente metálico | |
| `gold/shadow` | `#8B5E1A` | Shadow del gradiente, sombras del ícono | |
| `gold/line` | `#C9A227` | Línea divisoria entre wordmark y tagline | |

### Neutros
| Token | HEX | Uso |
|---|---|---|
| `ink/black` | `#0A0A0A` | Fondo dark, wordmark sobre blanco, ícono "G" Chrytsa | Negro suave (no #000) |
| `ink/pure` | `#000000` | Reserva para print CMYK 100K |
| `paper/white` | `#FFFFFF` | Fondo light, wordmark sobre negro variant |
| `paper/cream` | `#FAFAF8` | Fondo light alternativo (warmer) |

### Gradiente oro canónico (CSS)
```css
.gold-gradient {
  background: linear-gradient(135deg,
    #F4D773 0%,    /* highlight */
    #D4AF37 35%,   /* primary */
    #B8862B 70%,   /* mid */
    #8B5E1A 100%   /* shadow */
  );
}
```

---

## Tipografía extraída

### Wordmark "GRUPO CHRYTSA" / "HUYGHU & ASOCIADOS"
- **Familia**: serif clásico humanista mayúsculas
- **Características visibles**:
  - Remates triangulares angulares (no rectangulares)
  - Contraste alto entre asta gruesa y trazo fino
  - `R` con pierna curvada elegante
  - `G` con barra horizontal
  - `Y` con asta inclinada simétrica
- **Candidatos probables (orden de probabilidad)**:
  1. **Trajan Pro** (Adobe) — la opción más probable por el carácter clásico romano
  2. **Cinzel** (Google Fonts, libre) — alternativa open-source perfecta para web
  3. **Cormorant Garamond** (Google Fonts) — más caligráfico, menos probable
  4. Optima — descartado (es semi-serif)
- **Recomendación canónica**:
  - Print/PDF: **Trajan Pro Regular** (si Carlos tiene licencia Adobe)
  - Web/Email/Digital: **Cinzel Regular/Bold** (Google Fonts, embebible gratis)
  - Fallback stack: `'Trajan Pro', 'Cinzel', 'Cormorant Garamond', Georgia, serif`

### Tagline "ASESORES" / "CONTADORES PÚBLICOS"
- **Familia**: sans-serif geométrico con **tracking amplio** (letter-spacing ~0.3em)
- **Características**:
  - Mayúsculas
  - Peso medium (no bold)
  - Letras anchas, geométricas
- **Candidatos**:
  1. **Montserrat Medium** (Google Fonts) — la más probable
  2. Futura Medium
  3. Avenir Next Medium
- **Recomendación canónica**:
  - **Montserrat Medium** con `letter-spacing: 0.3em; text-transform: uppercase`
  - Fallback stack: `'Montserrat', 'Avenir Next', 'Futura', sans-serif`

### Body / UI / documentos internos
- Mantener **Inter** o **Manrope** para cuerpo (legibilidad pantalla)
- Migrar HUYGHU histórico (Arial) → Inter Regular 11pt
- Fallback stack: `'Inter', 'Manrope', system-ui, sans-serif`

---

## Sistema de símbolos (íconos)

### Grupo Chrytsa — Símbolo "G coronada"
- Letra **G** mayúscula en serif (mismo que wordmark)
- En variante fondo blanco: G negra
- En variante fondo negro: G blanca
- **Sobre la G**: arco/corona dorada con dos elementos cruzados que forman una "cresta" → sugiere coronación, jerarquía, holding
- Estilo: heráldico minimalista, banca de inversión

### HUYGHU & Asociados — Símbolo "Esfera fragmentada"
- Esfera/globo en gradiente oro y negro
- 4-5 bandas horizontales que segmentan la esfera con efecto 3D
- Mitad izquierda oro (luz), mitad derecha negra (sombra)
- Lectura simbólica: globalidad + estructura contable (líneas como filas de libro mayor) + dualidad luz/sombra (transparencia fiscal)

### Relación visual
- El símbolo Chrytsa (**G coronada**) es la marca paraguas
- El símbolo HUYGHU (**esfera**) es la submarca contable
- Comparten: oro idéntico, negro idéntico, layout circular, serif idéntico, underline oro idéntico

---

## Variantes a producir en el brand kit

Para cada marca (Chrytsa + HUYGHU):
1. Variante **light** (fondo blanco/cream + elementos negro/oro)
2. Variante **dark** (fondo negro + elementos blanco/oro)
3. Variante **monochrome black** (solo negro, para print BW)
4. Variante **monochrome gold** (solo oro, para foil stamping)
5. Variante **ícono solo** (sin wordmark, cuadrado, para avatars 1:1)
6. Variante **wordmark solo** (sin ícono, horizontal, para headers)

---

## Composición canónica

```
┌──────────────────────────────────┐
│            [ÍCONO]                │   ← 40% altura
│                                   │
│      G R U P O   C H R Y T S A    │   ← serif Trajan/Cinzel ~28pt
│      ─────────────────────────    │   ← línea oro 1px
│         A S E S O R E S            │   ← Montserrat Medium tracking 0.3em ~11pt
└──────────────────────────────────┘
```

Proporciones (canvas 1500×1500):
- Ícono: ocupa ~30-40% del canvas, centrado horizontalmente, ~25% del top
- Wordmark: 100% width, centrado, ~58% del top
- Línea oro: width = wordmark width × 1.05
- Tagline: centrado bajo la línea, ~72% del top
