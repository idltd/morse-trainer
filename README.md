# Morse Code Trainer

An interactive Morse code trainer styled after a classic PCB training board. Learn the international Morse alphabet by navigating a dichotomic search tree — the same binary tree used by radio operators for over a century.

Built as a Progressive Web App: install it on your phone, use it offline.

## How It Works

The tree encodes every letter of the alphabet. Starting from the root, each **dit** (short tap) branches left and each **dah** (long press) branches right. Every path through the tree lands on a letter.

```
              ●
           ·/   \—
          E       T
        ·/ \—   ·/ \—
       I    A   N    M
      ...  ...  ...  ...
```

The bottom row holds the full 26-letter alphabet. Numbers 0–9 extend to a fifth level and are shown in a reference panel.

## Modes

| Mode | What happens |
|------|-------------|
| **Explore** | Free play. Tap the key to navigate the tree and build words. Tap any node to hear its code. |
| **Encode** | A target letter pulses on the tree. Tap its Morse code on the key. |
| **Decode** | Hear a Morse sequence. Tap the same code back. Correct = green, wrong = red with the answer shown. |

## Controls

- **Touch key** — short tap = dit (·), long press = dah (—)
- **Keyboard** — spacebar (hold for dah), or type `.` and `-` directly
- **Click a node** — hear its Morse code played back
- **Backspace** — clear current input

## Running Locally

Double-click `00-startup.bat` or:

```
python -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000). Landscape orientation recommended.

## Installing as an App

On Android Chrome: menu → **Add to Home Screen**. The app works fully offline once installed.

## Architecture

Single-page PWA — everything in one HTML file with inline CSS and JS:

| File | Purpose |
|------|---------|
| `index.html` | Complete app — tree rendering, audio engine, game logic |
| `manifest.json` | PWA manifest for installability |
| `sw.js` | Service worker for offline caching |

**Audio**: Web Audio API generating 650 Hz sine tones — 120 ms for dit, 360 ms for dah.

**Tree**: SVG with computed node positions. Four levels for the 26 English letters; numbers at level five shown as a reference table.

## License

[GNU Affero General Public License v3.0](LICENSE) — free to use, modify, and distribute. Derivative works, including those offered as a network service, must be released under the same license.
