# Half Marathon Strength Tracker

A single-file, installable PWA for tracking an 8-week half marathon training block that pairs running with functional strength work. No build step, no backend — everything runs and saves locally in the browser.

## Features

- **Weekly schedule view** — 5 training days / 2 rest days, with each day's run and/or strength session laid out and checkable.
- **Three functional strength days**
  - **Day A — Squat & Power** (Monday)
  - **Day B — Posterior Chain & Stability** (Wednesday)
  - **Day C — Functional & Runner's Core** (Friday, paired with the tempo run)
- **Per-exercise weight logging** — log the weight used for each lift, saved between sessions so you can track progressive overload.
- **Exercise demo GIFs** — tap any exercise to see a demo animation full-screen. Real exercise GIFs are pulled from a public dataset, with an automatic fallback to a lightweight built-in animation if a clip fails to load (e.g. no signal at the gym) or has no dataset match.
- **8-week long run progression** — visualized as a winding track showing the week-by-week distance build (including the deload and taper weeks).
- **Installable as a PWA** — add to your iOS/Android home screen and use it like a native app, fully offline after first load (aside from the demo GIFs, which need a connection).

## Tech stack

- Vanilla HTML/CSS/JS — one file, no framework, no build step
- `localStorage` for all persistence (schedule checkmarks, logged weights, long run progress)
- Deployed as a static site (e.g. Netlify)

## Getting started

This is a single static file — no install, no dependencies.

**Run locally:**
```bash
# just open it
open index.html
```

**Deploy (Netlify):**
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag `index.html` onto the page
3. Netlify gives you a live URL immediately

> Note: iOS 18.5+ blocks JavaScript in local `file://` HTML, so for use as an installed PWA on iPhone it needs to be served over HTTPS (Netlify or similar) rather than opened directly from disk.

**Install as a PWA on iOS:**
1. Open the deployed URL in Safari
2. Tap the Share icon → **Add to Home Screen**
3. Launch it from the home screen icon like any other app

## Training schedule

| Day | Session |
|---|---|
| Mon | Strength A (Squat & Power) + Easy Run |
| Tue | Intervals |
| Wed | Strength B (Posterior Chain & Stability) |
| Thu | Rest |
| Fri | Tempo Run + Strength C (Functional & Runner's Core) |
| Sat | Long Run |
| Sun | Rest |

Long run progression: 5 → 6 → 7 → 5 (deload) → 8 → 9 → 10 → 7 (taper) miles over 8 weeks.

## Data & privacy

All data (checkmarks, logged weights, progress) is stored only in your browser's `localStorage` — nothing is sent to a server. Clearing site data/cache will reset your progress.

## Credits

Exercise demo GIFs are sourced from [hasaneyldrm/exercises-dataset](https://github.com/hasaneyldrm/exercises-dataset). That media is © [Gym visual](https://gymvisual.com/), redistributed by that repository with attribution required. This project displays that attribution in-app. If you plan to reuse the media beyond personal use, check Gym visual's own terms first.

## License

The code in this repository is available under the MIT License. Exercise demo media is licensed separately — see [Credits](#credits) above.
