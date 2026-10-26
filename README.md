# ·— ·—·· ·——· ···· ·— -··· · -

# Morse Code Trainer

[![Live App](https://img.shields.io/badge/PLAY_NOW-idltd.github.io-c8a84a?style=for-the-badge&logo=github)](https://idltd.github.io/morse-trainer/)
[![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue?style=for-the-badge)](LICENSE)
[![PWA Ready](https://img.shields.io/badge/PWA-Installable-22ff44?style=for-the-badge&logo=googlechrome&logoColor=white)](https://idltd.github.io/morse-trainer/)

---

**Can you tell a dit from a dah?** This browser-based trainer teaches you Morse code the way radio operators have learned it for over a century — by navigating a binary tree. Every letter is a path: go left for dit, go right for dah.

**[Launch the trainer](https://idltd.github.io/morse-trainer/)** — works on your phone, tablet, or desktop. Install it as an app and practise offline.

---

## The Tree

```
                    ●
                 ·/   \—
               E         T
            ·/ \—      ·/ \—
           I    A      N    M
          / \  / \    / \  / \
         S  U R  W  D  K G  O
        ···        ···        ···
       H V F    L   P J  B X C Y  Z Q
```

Start at the top. Short tap (dit) goes left. Long press (dah) goes right. Land on your letter. That's it.

Numbers (0–9) follow the same logic but go five levels deep — they're shown in a quick-reference panel so you don't need to memorise the tree.

## Three Ways to Practise

| | Mode | You do | The app does |
|---|------|--------|-------------|
| **1** | Explore | Tap freely | Shows where you are in the tree, builds decoded text |
| **2** | Encode | Tap the Morse code | Picks a letter and highlights it — get it right or see the answer |
| **3** | Decode | Listen, then tap it back | Plays a Morse sequence — you reproduce it |

## Controls

| Input | Dit (·) | Dah (—) |
|-------|---------|---------|
| Touch key | Short tap | Long press |
| Keyboard | `.` key | `-` key |
| Spacebar | Short press | Hold |

Click any letter on the tree to hear how it sounds. Backspace clears your current input.

## Get It On Your Phone

1. Open **[idltd.github.io/morse-trainer](https://idltd.github.io/morse-trainer/)** in Chrome
2. Rotate to **landscape**
3. Tap the menu → **Add to Home Screen**
4. Done — it works offline

## Under the Hood

One HTML file. No frameworks. No build step. Just open it.

| | |
|---|---|
| **Audio** | Web Audio API — 650 Hz sine wave, 120 ms dit, 360 ms dah |
| **Display** | SVG tree with computed positions, CSS for the PCB aesthetic |
| **Offline** | Service worker caches everything on first load |
| **Size** | ~20 KB total |

## Roadmap

- **Words & Messages** — a mode for practising full words and sentences, not just individual letters. Built-in word lists graded by difficulty.
- **Adaptive Training** — structured practice sessions that adjust difficulty based on your performance. Set goals, take tests, track progress.
- **Weakness Targeting** — track your error rate per letter and weight practice toward the ones you struggle with. Spaced repetition so problem letters come back until they stick.

Pull requests welcome on any of these.

## License

**AGPL-3.0** — Use it, fork it, improve it. But if you host a modified version as a service, you must share your source code too. That's the deal.

---

*-··· · · ·——· &nbsp; -··· · · ·——· &nbsp; -··· · · ·——·*
