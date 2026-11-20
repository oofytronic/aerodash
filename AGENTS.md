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

## Identities (read before linking, crediting or naming anything)

The author works under separate identities. Keep them straight:

- **Oofytronic**: the tech persona (`oofytronic-site`).
- **Feathermode**: the tech business (`feathermode-web`). It has customers, so it is the identity to protect most.
- **R. H. Sattaur**: the author persona (`rhsattaur`, the Somium Solest site, the stories). Fiction lives on the sites; the
  author's non-fiction lives elsewhere.
- **Remain Human by R. H. Sattaur** (`remainhuman.me`, its own repo): essays and audio on philosophy, history, culture,
  religion and economics, including American history and culture. It may be controversial.

Rules:

1. **Only `rhsattaur` links to Remain Human** (nav, home section and footer). No other site links to it, mentions it or
   borrows its themes. Ask first before adding any other link.
2. **Oofytronic and Feathermode do not link to, credit or mention** R. H. Sattaur, Remain Human or Somium Solest, and the
   author sites do not link to them, unless a link already exists. Ask before adding a new cross-link between any two identities.
3. Do not put the author's private email address, or any personal details, in public pages, commits or external requests.
4. Do not invent biography, lore or copy for any identity; ask when text was not supplied.
5. Do not share accounts, analytics or contact details between identities. Remain Human gets its own repo and hosting
   account; ask which GitHub account before creating it.
