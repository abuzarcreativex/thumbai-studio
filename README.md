# ThumbAI Studio — AI Thumbnail & Title Studio for Creators

**Built for IceHacks 2026** (CodeStarters, Devpost). Tracks: **AI & ML** + **Design & Craft**.

Type a video topic and ThumbAI Studio generates five CTR-scored video titles,
three opening hooks and five thumbnail text ideas — then lets you design a real
1280×720 thumbnail on a live canvas and download it as a PNG.

## What it does

- **AI titles** — five titles from proven formulas (curiosity gap, how-to,
  listicle, bold claim, question, …), each with a CTR score computed from
  length, power words, numbers, questions and year — plus the formula used.
- **Opening hooks** — three first-5-seconds lines written around your topic.
- **Thumbnail text ideas** — five punchy 2–4 word options; click one to use it.
- **Live thumbnail editor** — real 1280×720 canvas: 8 gradient backgrounds,
  solid colours, upload-your-own photo, 4 fonts, size slider, colours, outline
  toggle, 9 text positions, badge, arrow and circle highlight.
- **Thumbnail score** — live metrics: text length, word count, real contrast
  ratio (sampled from the actual background under the text), text coverage,
  overall 0–100 score with a grade (A–D) and concrete improvement tips.
- **One-click templates** — Bold Gamer, Clean Educator, Viral Vlog, Money Moves.
- **My Creations** — generations saved in localStorage; click to reload.
- **Copy buttons** on every generated item; **Download PNG** exports the real
  1280×720 canvas.

## How the "AI" works

The engine runs **entirely on-device in the browser** — no backend, no API
keys, no data leaves the device. It analyses the topic (keyword extraction,
stop-word filtering), slots the keywords into proven title/hook formulas
(ranked by the selected tone), and scores every title with a transparent
formula. The thumbnail score samples the real canvas pixels under the text
to compute a true WCAG contrast ratio.

## Run it

```bash
# any static server works, e.g.:
python3 -m http.server 8090
# then open http://localhost:8090/
```

Deploy: drop the folder on Vercel (or any static host) — `index.html` is the
whole app, zero build step, zero dependencies.

## Files

- `index.html` — the entire app (HTML + CSS + JS, self-contained)
- `test/verify.mjs` — Playwright end-to-end verification
- `test/screenshots/` — verification screenshots

## Disclosure

Built with Muse (AI coding assistant) for IceHacks 2026. The in-app AI engine
is a built-in, on-device generator — no external AI API is called.
