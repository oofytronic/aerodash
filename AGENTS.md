# Notes for agents and new contributors

Read `README.md`, then `design.md`. This is a single static page; the design is the old Feathermode page (parchment
palettes) and was deliberately kept.

## Rules

1. Work on `trunk`; push to `trunk`. No other branches, no pull requests unless asked.
2. No build tooling, frameworks or libraries. Edit the HTML, CSS and JS directly.
3. Semantic HTML, CSS custom properties for every colour, size and space (the tokens at the top of `css/style.css`),
   functional-leaning vanilla JavaScript.
4. Accessibility: keep the skip of motion under `prefers-reduced-motion`, visible focus styles, `aria-label`s on the
   nav and the theme toggle, and `role="status"` on the form hint.
5. Both palettes (`parchment-light`, `parchment-dark`) must keep working; test each.
6. **Copy must stay true to the promises:** end-to-end encrypted, local-first, user-owned, user-operated,
   relay-driven, privacy-first, for creators, consumers and curators. Do not add claims (features, prices, dates,
   comparisons with named companies) that the author has not given you.

## Traps

- There is no lock screen or password: the page removed it and is open to everyone. Do not add one back without being asked.
- The inline `<script>` in `<head>` sets `data-palette` before first paint; keep it, or the page flashes the wrong theme.
- The localStorage key is `ad-theme`. The waitlist form is a Netlify form named `aerodash-waitlist`
  (the `name`, the hidden `form-name` and the string in `js/main.js` must match).
- The CSS has one labelled section per part of the page; the "How it differs" section uses the `contrast-*` classes
  (it was the "Pricing" section; the compare-table styles were removed).
- Pushing to `trunk` replaces what is live.
- Fonts load from Google Fonts (the one third-party request).
