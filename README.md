# Aerodash

The landing site for **Aerodash**, an **everything app** that is end-to-end encrypted, local-first, user-owned,
user-operated, relay-driven and private by default, made for **creators, consumers and curators**. Aerodash is a
product of Feathermode (see the `feathermode-web` repo), and Gondola, the distribution platform, is planned as a
mini-app that rides inside it.

This site began as the previous Feathermode site (the "publishing home you actually own" pitch, kept for a while in
`feathermode-web/communication/`). It was moved here and its text rewritten for Aerodash; the page design (parchment
palettes, Crimson Pro and DM Sans, rounded cards) is unchanged.

- Static HTML, CSS and vanilla JavaScript. **No build step, no dependencies.**
- A private preview: the page opens behind a soft **password screen** (see "Things to know").

## Quick start

```sh
git clone https://github.com/oofytronic/aerodash
cd aerodash
python3 -m http.server 8000
# open http://localhost:8000/
```

Deploying is "serve the repo root". The waitlist form uses **Netlify Forms** (`data-netlify`), so it only collects
sign-ups when the site is hosted on Netlify.

## What is where

```
index.html        the whole page: lock screen, header, hero, six sections, waitlist, footer
css/style.css     all styles (tokens for both palettes, then one labelled section per part of the page)
js/main.js        lock screen, light/dark theme, waitlist form
favicon.svg       favicon: transparent, switches colour with the browser's light or dark theme
favicon.ico       transparent fallback (16/32/48)
design.md         structure, look, content notes, to-do list
HISTORY.md        what changed and when
AGENTS.md         notes for AI agents / new contributors
```

## The page

1. **Hero:** "Aerodash. An everything app you actually own."
2. **Right now, it takes a dozen apps:** four cards (messengers, social platforms, creator platforms, cloud apps).
3. **One app. Six promises:** end-to-end encrypted, local-first, user-owned, user-operated, relay-driven, privacy-first.
4. **Built for three kinds of people:** creators, consumers, curators.
5. **A different way to run an app:** "the usual way" against "the Aerodash way", which mentions Gondola.
6. **Waitlist:** an email form, plus a small footer ("A Feathermode product").

## The look

Two palettes, set by `data-palette` on `<html>`: `parchment-light` (cream `#EDEADE` with deep blue `#16446F`) and
`parchment-dark` (`#1C1917` with `#66A5E1`). An inline script in `<head>` picks one before first paint from the saved
choice (`localStorage` key `ad-theme`) or the system setting, so nothing flashes. Type is Crimson Pro (headings) and
DM Sans (text), loaded from Google Fonts. Corners are rounded, with soft shadows.

## Common tasks

| I want to… | Do this |
| --- | --- |
| Change the wording | Edit `index.html`. Every section is a plain `<section>` with an id the nav links to. |
| Change or remove the password screen | The password is stored only as a SHA-256 hash in `LOCK_HASH` in `js/main.js`. Make a new one with `printf 'the password' \| sha256sum`. To remove the screen, delete the `#lockScreen` block in `index.html`, the lock code at the top of `js/main.js`, and the `data-locked` lines in the `<head>` script. |
| Make the waitlist work somewhere else | The form posts to `/` for Netlify. Point `fetch('/', …)` in `js/main.js` (and the form's `action`) at your form service. |
| Change the logo | The mark is inline SVG in three places in `index.html` (lock card, header) and in `favicon.svg`. It is a placeholder: a ring with three speed lines. |

## Workflow

Work on **`trunk`** and push to `trunk`. No other branches are published. An `experimental` branch will be added when
asked for.

## Things to know

- **The lock screen is not security.** This is a static site, so the page's content ships to every visitor whether or
  not they enter the password; the hash only keeps the plaintext password out of view-source. It is carried over
  unchanged from the old site, so it is the same password. Remove it when the site goes public.
- The localStorage keys changed from `fm-*` to `ad-*` (`ad-theme`, `ad-unlocked`), so people unlocked on the old
  site must enter the password again.
- The Aerodash mark and the copy are new and are a first draft for the author to review. The name is unchecked for
  trademarks and domains.
- The "Compare" table of the old site (Feathermode against Books.by and Shopify) and its "Pricing" section were
  removed; the pricing layout is reused for "A different way to run an app".
- Tested only in headless Chromium (320 to 1920 wide, both palettes); not on real devices or with a screen reader.

See `design.md` for the to-do list and `HISTORY.md` for how the site got here.
