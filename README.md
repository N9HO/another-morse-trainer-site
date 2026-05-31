# Another Morse Trainer — website

Landing page for **Another Morse Trainer**, a modern Morse code (CW) trainer for iPhone.

> Learn Morse. Hear Progress.

Static site — plain HTML/CSS, no build step. Deployed with GitHub Pages.

## Local preview

```sh
python3 -m http.server 4178
# open http://localhost:4178
```

## Structure

| File | Purpose |
|------|---------|
| `index.html` | The whole page |
| `styles.css` | Navy / teal / white theme, responsive layout |
| `assets/mark.png` | Logo symbol (background keyed to transparent) |
| `assets/logo-stacked.png` | Stacked logo (symbol + wordmark) for the footer |
| `assets/icon.svg` | App icon, used as the favicon |

## Brand

- **Deep CW Navy** `#071B34` · **Teal Signal** `#27D3E8` · **White** `#FFFFFF`
- Accents: Success Green `#34D399` · Warning Amber `#F59E0B` · Error Red `#EF4444`
- Type: **Inter** (UI) · **JetBrains Mono** (code / Morse)

The app itself is a native SwiftUI iOS app — see
[N9HO/another-morse-trainer](https://github.com/N9HO/another-morse-trainer).
