# Another Morse Trainer — website

Landing page and user guide for **Another Morse Trainer**, a modern Morse code
(CW) trainer for **iPhone and Android**.

> Learn Morse. Hear Progress.

Static site — plain HTML/CSS, no build step. Deployed with GitHub Pages at
[anothermorsetrainer.app](https://anothermorsetrainer.app).

## Local preview

```sh
python3 -m http.server 4178
# open http://localhost:4178
```

## Structure

| File | Purpose |
|------|---------|
| `index.html` | Landing page — hero, features, all 20 modes grouped by purpose |
| `guide/index.html` | The user manual: every mode, setting, and hardware option |
| `privacy/index.html` | Privacy policy (linked from both app store listings) |
| `styles.css` | Navy / teal / white theme, responsive layout, guide layout |
| `assets/mark.png` | Logo symbol (background keyed to transparent) |
| `assets/logo-stacked.png` | Stacked logo (symbol + wordmark) for the footer |
| `assets/icon.svg` | App icon, used as the favicon |

## The guide

`guide/` is the app manual, kept in sync with what's actually shipped in the two
app repos. It's organised as:

- **Basics** — getting started, how Koch / time-to-recognize / Farnsworth work,
  the home screen, running a session, the four ways to answer
- **The modes** — all twenty, grouped: learn the characters · copy real content ·
  build speed · get on the air · send, decode & look up
- **Reference** — progress & stats, every setting, hardware keys, troubleshooting

When a mode is added or renamed in either app, update the matching section here
and the mode grid on `index.html`.

## Store badges

The App Store and Google Play badges in the hero are intentionally **not links** —
they carry a "Coming soon" ribbon while both apps are in testing. When a listing
goes live, wrap the relevant `.store-badge` in an `<a href="…">`, drop its
`.sb-soon` span, and remove the `opacity` by deleting the badge's disabled
styling. The paragraph below them (`.store-note`) should be updated at the same
time.

## Brand

- **Deep CW Navy** `#071B34` · **Teal Signal** `#27D3E8` · **White** `#FFFFFF`
- Accents: Success Green `#34D399` · Warning Amber `#F59E0B` · Error Red `#EF4444`
- Type: **Inter** (UI) · **JetBrains Mono** (code / Morse)

## The apps

- **iOS** — native SwiftUI:
  [N9HO/another-morse-trainer](https://github.com/N9HO/another-morse-trainer)
- **Android** — Kotlin + Jetpack Compose:
  [N9HO/another-morse-trainer-android](https://github.com/N9HO/another-morse-trainer-android)
