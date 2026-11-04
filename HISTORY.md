# History

## From the old Feathermode site to Aerodash (6 Nov 2026)

- **Origin.** The site started life as the Feathermode site: a pitch for a user-owned writing and self-publishing
  platform (novels, serial fiction, nonfiction, manga; storefront, reader support tiers, a shared discovery registry,
  built-in newsletters), in parchment palettes with Crimson Pro and DM Sans, behind a soft password screen. When
  Feathermode became the parent site (25 Oct 2026) that page was set aside unchanged in `feathermode-web/communication/`.
- **Naming.** The communication / everything-app product was called Common Tongue, then renamed **Aerodash**
  (31 Oct 2026). Its distribution platform, Airlift, became **Gondola** and was described as a mini-app that rides
  inside Aerodash.
- **This repository.** The old page was copied here (HTML, CSS and JavaScript, design unchanged) and the text was
  rewritten for Aerodash: an everything app that is end-to-end encrypted, local-first, user-owned, user-operated,
  relay-driven and privacy-first, for creators, consumers and curators.
  - New hero, "right now it takes a dozen apps", six promises, three audiences, and "a different way to run an app".
  - The Books.by/Shopify comparison table and the pricing section were removed (the layout of the pricing section
    now holds the "usual way vs Aerodash way" columns).
  - A new Aerodash mark (a ring with three speed lines) and a transparent, theme-aware favicon replaced the Feathermode feather.
  - localStorage keys renamed `fm-*` to `ad-*`; the Netlify form renamed `aerodash-waitlist`; footer now says
    "A Feathermode product".
  - The password screen and its hash were kept as they were.

## Decisions to remember

- Keep the original design: it is the Feathermode look, and Aerodash is a Feathermode product.
- Work on `trunk` only; an `experimental` branch comes later when asked for.
- The lock screen is a soft preview gate, not security.

## Not done yet

See `design.md` (to-do list).
