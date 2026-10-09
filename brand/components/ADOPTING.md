# Bringing the palette into the dashboard

The palette (`index.html`) is the spec for the Cleo dashboard's look. It is static
HTML, so it settles how things look but not how they move. This page covers how the
dashboard adopts it.

## Golden rules

1. **Design holistically and elegantly, with zen.** Each change should leave the whole
   system simpler, not just one screen prettier.
2. **Delete before adding.** Prefer a systemic improvement to an additive one. A
   restyled component replaces its duplicates and the one-off styles around it, so most
   changes should remove more code than they add.
3. **Rebuild when it doesn't fit.** If a component or page needs a major change to match
   the palette, rebuild it to the spec rather than patching classes until it is close.
   "Close enough" is not done.

## Order of work

0. **Delete dead UI.** Remove components nothing imports, and the packages only they
   used. No visual change, so it is easy to review and shrinks what has to be restyled.
1. **Tokens.** Port the palette's colours (Cleo Blue primary, neutral greys, status set,
   chart palette), radii, shadows and easing into the dashboard's central theme. Most of
   the visual change lands here, in one place, in both themes.
2. **Primitives.** Restyle each shared component to the palette and fold its duplicates
   into it: status pills replace ad-hoc badges, one tracing mark replaces every spinner,
   the blue primary button replaces black ones. Keep component APIs stable where you can,
   and remove per-file `dark:` overrides and raw hex values as you go.
3. **Brand.** The mark gets its variants (full colour, white, mono) and its two motions
   (draw-on, tracing), both stopped under reduced motion.
4. **Patterns.** Move pages onto the nine page patterns one at a time, deleting each
   page's bespoke layout as it moves. Start with the most-used screens: home (the Today
   layout) and the inbox.
5. **Guardrails.** A design-system route that renders the real components replaces this
   static page as the living reference, with screenshot tests in CI, and a check that
   fails on new raw hex colours, `dark:` overrides and one-off spinners.

Each step is judged against the palette page side by side.

## Behaviour: what the mock can't show

Hover and press feedback, sliding tab indicators, rows that expand smoothly and toasts
that stack all need real interaction code. For those, use
[EasyUI](https://easyui.site/) (MIT, added through the shadcn CLI, built on Framer Motion)
as the starting point for behaviour, then restyle to Cleo's tokens. The copied code is
ours to edit and replaces our existing version.

| Component | Starting point |
| --- | --- |
| Tabs, expandable table row, undo toast, split button, command menu, checkbox | EasyUI's version, restyled |
| Select, dialog, popover, tooltip, menus | our existing Radix components, restyled (they carry keyboard and accessibility behaviour) |
| Recording player, transcript, live call card, agent settings rows | built new from the palette |

Leave out the showpiece effects (gooey menu, neon edge button, liquid toggle). They pull
against the calm the palette is aiming for.
