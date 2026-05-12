# Brand Palette — Chrytsa & HUYGHU

Paleta canónica oficial. **No modificar** sin aprobación del Brand Manager.

## Colores Primarios

| Token | HEX | RGB | CMYK | Pantone | Uso |
|-------|-----|-----|------|---------|-----|
| **Oro Canónico** | `#D4AF37` | 212 175 55 | 12 28 87 5 | 871 C (Metallic) | Logo principal, accents, CTAs |
| **Negro Corporativo** | `#0A0A0A` | 10 10 10 | 0 0 0 96 | Black 6 C | Fondos, body text negativo |
| **Marfil Premium** | `#F6F0E3` | 246 240 227 | 0 2 8 4 | 9043 C | Body text positivo, papel |

## Gradiente Oro Oficial

Stops oficiales del gradiente canónico (lineal 135°):

```
0%   #F4D773  (oro claro · highlight)
35%  #D4AF37  (oro canónico · base)
70%  #B8862B  (oro medio · sombra)
100% #8B5E1A  (oro oscuro · profundidad)
```

CSS:
```css
background: linear-gradient(135deg, #F4D773 0%, #D4AF37 35%, #B8862B 70%, #8B5E1A 100%);
```

## Colores Secundarios

| Token | HEX | Uso |
|-------|-----|-----|
| Gold Light | `#F4D773` | Headlines, highlights premium |
| Gold Dark | `#8B5E1A` | Hover states, sombras texto |
| Mute Light | `#bcb29a` | Body secundario sobre negro |
| Dim Gold | `#8a7f6a` | Footer, micro-text, dim labels |
| Border Gold | `rgba(212,175,55,.18)` | Bordes sutiles, separadores |
| Paper Dark | `#181614` | Cards sobre negro |
| Surface Dark | `#141414` | Surfaces secundarias |

## Funcionales

| Token | HEX | Uso |
|-------|-----|-----|
| Success | `#1F8A5B` | Confirmaciones DGII, pagos OK |
| Warning | `#D97757` | Recordatorios vencimiento |
| Error | `#B83A26` | Errores críticos (uso limitado) |

## Reglas de Uso

1. **Oro #D4AF37 es exclusivo de elementos de marca y CTAs**. No usar en body text largo.
2. **Negro #0A0A0A es el fondo institucional canónico**. Variantes #141414 y #181614 sólo para layering.
3. **Contraste mínimo AA**: oro sobre negro = 8.4:1 ✓ · marfil sobre negro = 16.8:1 ✓
4. **Pantone Metallic 871 C** es obligatorio para impresión de tarjetas Touche Cover 350g + UV selectivo.
5. **No combinar oro con otros amarillos**. El oro canónico es el único acento dorado del sistema.

## Tipografía aparejada

- Headlines display → **Cinzel** (Google Fonts)
- Body & UI → **Inter** (Google Fonts)
- Quotes / itálicas → **Cormorant Garamond** (Google Fonts)
- Tracking labels → **Montserrat** (Google Fonts)
- Code / meta → **JetBrains Mono** (Google Fonts)

---

**v1.0** · Bloqueada oficialmente · Diciembre 2026
