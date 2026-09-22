# assets

Public brand and marketing artwork for Cleo, served over jsDelivr so that
email clients and third-party tools can load it from an absolute URL.

```
https://cdn.jsdelivr.net/gh/Aiva-Labs-AI/assets@main/<path>
```

## `email/`

Artwork for the email blast template in
[`cleo-internal-ai`](https://github.com/Aiva-Labs-AI/cleo-internal-ai)
(`email/`). Raster only — email clients don't render SVG.

| file | display size | used for |
| --- | --- | --- |
| `hero-banner.jpg` | 600×300 | hero banner (1200×600 source, retina) |
| `hero-banner.png` | — | uncompressed master for the hero |
| `logo-white.png` | 120 wide | full lockup on dark backgrounds |
| `logo-dark.png` | 120 wide | full lockup on light backgrounds |
| `icon-colored-128.png` | 42×42 | signature avatar |
| `icon-colored-512.png` | — | spare colored mark |
| `icon-white-512.png` | — | spare white mark |
| `icon-colored.svg` | — | vector mark, for web not email |
| `poster-demo.jpg` | 544×306 | video poster with play button, links to YouTube |
| `social-linkedin.png` | 24×24 | footer social icon |
| `social-mail.png` | 24×20 | footer social icon |

jsDelivr caches a path aggressively: overwriting a file on `main` can take up
to 24 hours to propagate. Give a revised image a new filename instead.
