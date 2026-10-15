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
| `cleo-mark-mono.svg` | one colour (`currentColor`), back pieces at half strength; for status pills and other coloured fills |
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

### `logo/official/`

The designer's exported files from the 2026 Brand Guidelines, one file per
size. Prefer these over the reconstructions above wherever the exact artwork
matters (site, ads, decks, print).

| files | what |
| --- | --- |
| `cleo-logo-{48,64,96,128,256}.svg` | horizontal lockup, full colour, for light backgrounds |
| `cleo-logo-negative-*.svg` | horizontal lockup, white, for blue, black or photo backgrounds |
| `cleo-mark-{32,48,64,96,128,256}.svg` | logomark, full colour |
| `cleo-mark-negative-*.svg` | logomark, white |
| `cleo-logo-stacked-{64,96,128,192,256}.svg` | vertical lockup, full colour |
| `cleo-logo-stacked-negative-*.svg` | vertical lockup, white |

The number is the artwork's height in px (width for the stacked lockup).

### Logo usage

- **Primary logo:** the horizontal lockup, for most applications.
- **Backgrounds:** full colour on light surfaces; the white (`-negative`)
  version on Cleo Blue, black or photography.
- **On photos:** place the logo over calm, high-contrast areas with negative
  space, never over busy detail or faces.
- **Clear space**, measured in logomark heights: horizontal lockup 1/2 around
  it (1/6 between mark and wordmark); logomark alone 1/4; stacked lockup 1/3
  around it (1/8 between mark and wordmark). Nothing else goes inside it.
- **Minimum size:** horizontal lockup 145px wide, stacked lockup 32px wide,
  logomark 24px.
- **Don't:** change the typeface or colours, add effects or strokes, rotate
  it, or alter its proportions. Use the files as they are.

## `components/`

The component palette for the Cleo dashboard: open `components/index.html`
in a browser. See [`components/README.md`](components/README.md).

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

Photography gets a subtle dither treatment in Cleo's blue tones, so it reads as
a digital texture while the image stays recognisable. Patterns are built from
circles, lines and repeated structures; use them as supporting backgrounds
(decks, social, web) and never let them compete with the logo, type or
message.
