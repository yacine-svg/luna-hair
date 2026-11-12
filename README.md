# Luna Hair

Scroll-driven landing page for **Luna Hair**, an Algerian natural hair-growth oil ("Elixir for Long & Strong Hair", 60 ml).

Scrolling plays a 21.6-second product film forwards and backwards, with French titles fading in over each shot and a WhatsApp order button at the end.

## How it works

- The film is split into 250 WebP frames in `frames/` (1280×720, about 7 MB in total).
- `index.html` draws the frames on a `<canvas>` according to scroll position, easing toward the target frame and blending adjacent frames for smooth motion.
- Text beats are keyed to film progress via `data-in` / `data-out` attributes on each `.beat`.
- On tall phone screens, the film sits in the top 62% of the screen and the text sits below it.
- No build step and no dependencies: a static site (Google Fonts only).

## Files

| Path | What it is |
|---|---|
| `index.html` | The whole page: markup, styles and the scroll engine |
| `frames/f001.webp` to `frames/f250.webp` | Frames of the film, in order |
| `media/luna-scroll.mp4` | The source film (all-keyframe H.264, no audio) |
| `media/poster.jpg` | First frame, for social previews |

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000.

## To do before launch

- Replace the plain-text Instagram ("Luna magic hair") and Facebook ("Huile Luna") names with real profile links.
- Confirm the copy under "Soin naturel haut de gamme" and "Une goutte. Un rituel." with the client.
