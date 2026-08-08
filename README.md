# Kyasino88 Help Center

Bilingual (English / नेपाली) video-tutorial site for **Kyasino88** — download, register, deposit, withdraw, play, and refer & earn.

- One full tutorial video per topic with a designed play-thumbnail
- Step-by-step screenshots pulled straight from the official screen-records, under each video
- One-tap **EN ⇄ नेपाली** toggle — swaps all copy **and** the language-matched video + screenshots
- Emerald-and-gold Kyasino88 casino theme, motion/animation (scroll reveals, sheen CTAs, glow cards)
- Responsive, fully offline static site (no build step, no external JS)

## Guides
| Guide | Category | Steps |
|-------|----------|-------|
| How to Download | Get Started | 6 |
| How to Register | Get Started | 6 |
| How to Deposit (FonePay / bank QR) | Wallet | 7 |
| How to Withdraw | Wallet | 6 |
| How to Play | Playing | 6 |
| How to Refer & Earn | Rewards | 5 |

## Structure
```
index.html
assets/
  css/style.css        # emerald + gold theme
  js/content.js        # all bilingual copy + guide data (edit here)
  js/app.js            # SPA router, language toggle, motion
  img/
    logo-kyasino.png, logo-k88.png, app-icon.png
    steps/<guide>/step-NN.png       # English screenshots
    steps/<guide>/ne/step-NN.png    # Nepali screenshots
videos/<guide>-en.mp4 , <guide>-ne.mp4
```

## Run locally
Static site — serve the folder and open it:

```bash
py -m http.server 5199 --directory "D:/DonaldWork_2024/k88/k88-help-center"
```

Then open http://127.0.0.1:5199

## Editing content
All copy lives in `assets/js/content.js` (`links`, `ui.en` / `ui.ne`, `tutorials[]`).
Add or reword steps there — no code changes needed. Update the outbound links
(`download`, `play`, `telegram`, `facebook`, `liveChat`) to the live Kyasino88 URLs.
