# Design

The single page for **Aerodash**. It keeps the look of the old Feathermode page (Feathermode is the parent brand);
only the words and the mark changed.

## Purpose and voice

- Introduce Aerodash as an **everything app** that is end-to-end encrypted, local-first, user-owned, user-operated,
  relay-driven and privacy-first, made for **creators, consumers and curators**, and collect waitlist sign-ups.
- Voice: plain, calm, confident; short sentences; no jargon beyond the promises themselves; no hype.

## Structure (`index.html`)

1. Lock screen (soft preview gate), a decorative sky glow, a sticky header (mark, nav, theme toggle).
2. `#top` hero. 3. `#the-gap` "Right now, it takes a dozen apps". 4. `#how-it-works` six promises.
5. `#who-its-for` creators, consumers, curators. 6. `#difference` the usual way vs the Aerodash way (mentions Gondola).
7. `#waitlist` email form. 8. Footer: "Own it. Run it." and "A Feathermode product".

## Look

- Palettes: `parchment-light` (bg `#EDEADE`, accent `#16446F`) and `parchment-dark` (bg `#1C1917`, accent `#66A5E1`).
- Type: Crimson Pro (serif, headings) and DM Sans (text). Rounded corners (`--radius-*`), soft shadows.
- Mark: a ring with a filled centre and three speed lines (inline SVG, `currentColor`-style via `--color-accent`).
  It is a placeholder.
- Motion: a short fade-up on the hero, switched off under `prefers-reduced-motion`.

## Content notes

- The hero, the four "dozen apps" cards, the six promises, the three audiences and the contrast lists are a first draft
  written from the author's brief. Review them.
- No prices, dates or named-competitor comparisons are claimed (the old page's Books.by/Shopify table was removed).
- Gondola is mentioned once, as a mini-app, in "the Aerodash way".

## To do

- [ ] Review and edit the copy.
- [ ] A final Aerodash mark and a social preview image (Open Graph); canonical URL once the domain is known.
- [ ] Check the name Aerodash (trademarks, domain) before launch.
- [ ] A real waitlist backend if not hosted on Netlify.
- [ ] Self-host the fonts instead of using Google Fonts.
- [ ] Test on real devices and with a screen reader.
- [ ] Decide what happens to the old copy in `feathermode-web/communication/` (it is untouched there).
