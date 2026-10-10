# Cleo component palette

`index.html` is the component palette for the Cleo dashboard: every component
drawn live in the Cleo brand kit, in light, off-white and dark. Open it in a browser; it
is a single self-contained page (fonts load from Google Fonts).

Groups:

| group | what |
| --- | --- |
| 00 Foundations | colour ramps and semantic roles, type scale, spacing, radius, elevation, motion (draw-on and tracing), mark variants, icons |
| 01 Primitives | buttons, inputs, selects, checkboxes, switches, segmented controls, sliders, date range, pills, chips, avatars, tooltips |
| 02 Navigation | sidebar, top bar, breadcrumb, tabs, settings navigation, pagination, stepper |
| 03 Data display | KPI cards, data table, cards, lists, charts, heatmap, funnel, meters, timeline, schedule, empty and loading states |
| 04 Calls & conversations | recording player, transcript, AI summary, call path, message thread, composer, conversation list, customer, vehicle and service history, live call bar, notifications |
| 05 Overlays & feedback | dialog, side sheet, menus, filter popover, command palette, toasts, callouts, coachmark, save bar |
| 06 Page patterns | dashboard, list + sheet, three-pane inbox, master–detail, settings, wizard, today (operational home), agent configuration, filter bar, sign in |

Tokens are the CSS custom properties at the top of the page (`--blue`,
`--surface`, `--ink`, `--s4`, `--r-lg`, `--e2` …). Colours come from
[`../colors/palette.json`](../colors/palette.json); the mark from
[`../logo`](../logo). All names and figures on the page are example data.

This is a visual reference rather than a code library. [`ADOPTING.md`](ADOPTING.md) covers how the dashboard adopts it.
