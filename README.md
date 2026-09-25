# Half Marathon Strength Tracker

A single-file, installable PWA for tracking a 14-week half marathon training block that pairs running with functional strength work. No build step, no backend — everything runs and saves locally in the browser.

## Features

- **Weekly schedule view** — each day's run and/or strength session laid out and checkable.
- **Two full strength days plus a short core day** — built only around dumbbells, bench, chest/shoulder machines, leg curl/extension, cable (no lat pulldown), bike and treadmill. No barbell or racks required.
  - **Lift & Carry Strength** (Monday)
  - **Single-Leg Power & Stability** (Thursday)
  - **Core Reset — Posture, Breathing & Hips** (Wednesday, ~18 min active recovery)
- **Time-boxed sessions** — Lift & Carry and Single-Leg Power run as supersets and are built to fit a 70 minute gym visit (5 min warm-up, ~50 min work, 5 min cool-down). Each day shows its warm-up, superset format, rest periods and target time.
- **Functional carry-over** — every exercise names the everyday task it transfers to (carrying groceries, stairs with shopping, lifting luggage overhead), shown when you tap into the demo.
- **Per-exercise weight logging** — log the weight used for each lift, saved between sessions so you can track progressive overload.
- **Exercise demo GIFs** — tap any exercise to see a demo animation full-screen. Most clips come from a public dataset. Pogo hops, jump squats, and the machine shoulder press, chest press, and leg curl use local clips in `gifs/` because the dataset has no match. If a clip fails to load, the app falls back to a lightweight built-in animation.
- **14-week long run progression** — a scrolling winding track showing the week-by-week distance build through both deloads, the taper and race day.
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
2. Drag the project folder onto the page so `index.html` and `gifs/` deploy together
3. Netlify gives you a live URL immediately

> Note: iOS 18.5+ blocks JavaScript in local `file://` HTML, so for use as an installed PWA on iPhone it needs to be served over HTTPS (Netlify or similar) rather than opened directly from disk.

**Install as a PWA on iOS:**
1. Open the deployed URL in Safari
2. Tap the Share icon → **Add to Home Screen**
3. Launch it from the home screen icon like any other app

## Training schedule

| Day | Session |
|---|---|
| Sun | Rest, or a 15–20 min shakeout |
| Mon | Lift & Carry Strength |
| Tue | Intervals — VO2 max key session |
| Wed | Core Reset (~18 min) |
| Thu | Single-Leg Power & Stability |
| Fri | Tempo Run |
| Sat | Long Run |

Long run progression: 5 → 6 → 7 → 5 (deload) → 7 → 8 → 9 → 10 → 11 → 8 (deload) → 12 → 10 → 8 (taper) → 13.1 (race) miles over 14 weeks.

Set the **Week 1 starts** date on the Progress tab to the day your block begins; the app derives the current week, and every run prescription, from it.

## Data & privacy

All data (checkmarks, logged weights, progress) is stored only in your browser's `localStorage` — nothing is sent to a server. Clearing site data/cache will reset your progress.

## Credits

Most exercise demo GIFs are sourced from [hasaneyldrm/exercises-dataset](https://github.com/hasaneyldrm/exercises-dataset). That media is © [Gym visual](https://gymvisual.com/), redistributed by that repository with attribution required. This project displays that attribution in-app. If you plan to reuse the media beyond personal use, check Gym visual's own terms first. Pogo hops, jump squats, machine shoulder press, machine chest press, and machine leg curl use the local files in `gifs/`.

## License

The code in this repository is available under the MIT License. Exercise demo media is licensed separately — see [Credits](#credits) above.
