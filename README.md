# Another Morse Trainer: website

Landing page and user guide for **Another Morse Trainer**, a modern Morse code
(CW) trainer for **iPhone and Android**.

> Learn Morse. Hear Progress.

Static site. Plain HTML/CSS, no build step. Deployed with GitHub Pages at
[anothermorsetrainer.app](https://anothermorsetrainer.app).

## Local preview

```sh
python3 -m http.server 4178
# open http://localhost:4178
```

## Structure

| File | Purpose |
|------|---------|
| `index.html` | Landing page: hero, features, all 28 modes grouped by purpose, a "Why I did this" note from the developer |
| `guide/index.html` | The user manual: every mode, setting, hardware option, and the FAQ covering how to get the app |
| `privacy/index.html` | Privacy policy (linked from both app store listings) |
| `styles.css` | Navy / teal / white theme, responsive layout, guide layout |
| `assets/mark.png` | Logo symbol (background keyed to transparent) |
| `assets/logo-stacked.png` | Stacked logo (symbol + wordmark) for the footer |
| `assets/icon.svg` | App icon, used as the favicon |

## The guide

`guide/` is the app manual, kept in sync with what's actually shipped in the two
app repos. It's organised as:

- **Basics**: getting started, how Koch / time-to-recognize / Farnsworth work,
  the home screen, running a session, the four ways to answer
- **The modes**: all twenty-eight (Daily Dit and the six arcade games among them), grouped as learn the
  characters · copy real content · build speed · get on the air · send, decode &
  look up
- **Reference**: progress & stats, every setting, hardware keys, troubleshooting

When a mode is added or renamed in either app, update the matching section here
and the mode grid on `index.html`.

## Store badges and availability

The two hero badges track where each app actually is:

| Badge | State | Markup |
|-------|-------|--------|
| TestFlight | iOS open beta, **live link** | `<a class="store-badge" href="…">` with `<span class="sb-soon live">Open beta</span>` |
| Google Play | Android closed testing, **not a link** | `<div class="store-badge">` with `<span class="sb-soon">Closed testing</span>` |

`a.store-badge` picks up full opacity and a hover lift; the plain `div` form stays
dimmed and non-interactive. When the Play listing goes public, swap the `div` for
an `<a href="…">`, change the ribbon to `class="sb-soon live"`, and update the
`.store-note` paragraph underneath. That's the sentence telling people iOS is
open and Android is invite-only via Discord.

Links used in the hero, nav, footer and guide FAQ:

- TestFlight: <https://testflight.apple.com/join/ZwXF88Gh>
- Discord: <https://discord.gg/qgyk3TPUd9>

Discord is the route to an Android closed-test invite, so it appears in the nav,
the community block on the landing page, the footer of every page, and the first
two answers in the guide's FAQ. If the invite is ever rotated, those are the
places to change.

## Brand

- **Deep CW Navy** `#071B34` · **Teal Signal** `#27D3E8` · **White** `#FFFFFF`
- Accents: Success Green `#34D399` · Warning Amber `#F59E0B` · Error Red `#EF4444`
- Type: **Inter** (UI) · **JetBrains Mono** (code / Morse)

## The apps

- Both apps live in one repository, [N9HO/another-morse-trainer](https://github.com/N9HO/another-morse-trainer):
  `ios/` (native SwiftUI) and `android/` (Kotlin + Jetpack Compose). Its `PARITY.md`
  is the rule that the two apps ship the same feature set, and its `CLAUDE.md`
  carries the rule that this guide changes in the same release as the app.
