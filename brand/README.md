# Cleo brand kit (vector)

Vector reconstruction of the Cleo brand sheet: logo, colours, type scale,
semantic icons and graphic elements. Everything is SVG with outlined text, so
nothing depends on installed fonts.

## `logo/`

| file | what |
| --- | --- |
| `cleo-mark.svg` | logomark with the sheet's shading (each band casts a soft shadow onto the gap and the piece beneath it) |
| `cleo-mark-flat.svg` | logomark without the shadow, for small sizes and print |
| `cleo-mark-negative.svg` | white mark for black or dark backgrounds |
| `cleo-logo.svg` / `cleo-logo-flat.svg` | horizontal lockup, mark + wordmark |
| `cleo-logo-stacked.svg` | stacked lockup |
| `cleo-wordmark.svg` | wordmark alone |
| `cleo-app-icon.svg` | app icon, 1024 grid |

Mark colours: front `#0057FF`, back `#0538CB`. The mark is one arm (a band and the
darker piece tucked under it) repeated at 90° steps, so it is exactly symmetric; the
shading is an SVG `feDropShadow` per arm (black, 24%, blur 2.45, offset toward the
arm's inside), which browsers, Figma and Illustrator render. Use the `-flat` files where
filters aren't supported. Wordmark: Geist SemiBold at
-3.3% tracking, `#000000`, cap height two thirds of the mark, gap 17% of the
mark.

## `colors/`

`palette.svg` (swatch sheet), `palette.json` and `palette.css` (tokens).

| name | hex |
| --- | --- |
| White | `#FFFFFF` |
| Mist | `#E6ECF5` |
| Cleo Blue | `#0057FF` |
| Royal | `#0538CB` |
| Navy | `#082549` |
| Ink | `#010516` |

Each colour has an eight-step ramp (`--cleo-<name>-100` … `-800`). The sheet
labels Cleo Blue `#2355F6`: that is its Display P3 value, which renders as
`#0057FF` in sRGB. The brand gradient runs Cleo Blue → Royal → Navy → Ink,
top to bottom.

## `typography/`

Geist (SIL OFL). `type-scale.json` has every style from the sheet; headings
are Regular at -2% tracking, paragraphs Regular or Medium at +2% and 60%
opacity. `type-specimen.svg` reproduces the sheet's type page.

## `icons/`

Momentum, Speed and Connection on a 24 grid with `currentColor`. Momentum and
Connection are Lucide's `repeat` and `workflow` at a 1.25 stroke; Speed is
traced from the sheet.

## `elements/`

Globe, waveform and four-circle line tiles (white at 50% on Cleo Blue) and the
brand gradient. The halftone car photography and the product UI collage on the
sheet are raster artwork and are not included.
