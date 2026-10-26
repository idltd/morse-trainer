# Morse Code Trainer

A PWA-based Morse code trainer styled after a physical PCB training board with a dichotomic search tree (binary tree where dit=left, dah=right).

## Features

- **Visual binary tree** showing the full Morse code alphabet with gold PCB-style traces
- **Interactive key** — short tap for dit (·), long press for dah (—), or use keyboard spacebar
- **Audio tones** via Web Audio API (650Hz sine wave)
- **Three modes:**
  - **Explore** — freely navigate the tree, tap nodes to hear their code
  - **Encode** — given a letter, tap the correct Morse code
  - **Decode** — hear a Morse sequence, identify the letter
- **PWA** — installable on Android/iOS, works offline

## Running Locally

Double-click `00-startup.bat` or run:

```
py -m http.server 8000
```

Then open http://localhost:8000.

## Architecture

Single-page PWA — all logic in `index.html` with inline CSS/JS:
- `index.html` — the full app
- `manifest.json` — PWA manifest for installability
- `sw.js` — service worker for offline caching

## Version

0.1.0 — Initial release
