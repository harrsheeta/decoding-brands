# PROMPT 58 — Sectors Collage EV Drone 5G (broll_idea_with_videos, 5.2 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (broll_idea_with_videos audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `broll_idea_with_videos_4K_sfx.mp4` (sound effects only) and `broll_idea_with_videos_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~5.2 s).

## Show look — "Decoding Brands" (Zero01 Network), China-brands episode
Ignore my saved Jet Airways / Meta / idk / dairy themes and any saved article rules; follow ONLY this look.
- **Watermarks on every frame:**
  - top-left: the "ZERO01⚡NETWORK" logo (small, ~22 px tall, 30 px from the edges; white on dark scenes, dark on light scenes)
  - top-right: the "DECODING BRANDS" yellow-green badge (~60 px)
- **Backgrounds** (each clip says which):
  - **Dark:** near-black #0B0B0B → #1A1A1A with a soft vignette.
  - **Cream:** #FBF4E6 with a very faint vertical line texture (thin lines ~4% darker, ~6 px apart, fading out toward the centre).
  - **White:** #FFFFFF.
  - **Desktop:** a macOS El Capitan / Yosemite sunset-mountain wallpaper.
- **Type:**
  - Neue Haas Grotesk / Helvetica Neue (fallback Inter) for body, labels and UI.
  - For big labels: a bold condensed sans (Bebas Neue / Barlow Condensed Bold) in caps, often with a small black italic "kicker" word above (e.g. *World's* / FACTORY).
- **Accent colours:** green #13875E (card borders, big labels), China red #D7262B, gold #F2B866.
- **Video cards:** rounded corners (~12 px) with a ~4 px green #13875E border on cream scenes; plain square tiles on dark scenes.
- **B-roll:** "b-roll" means short real video clips. Play them inside their cards/tiles; never use still frames when a clip is available.
- **Motion:** smooth, eased (ease-out quint, small overshoot on pops), with gentle constant camera drift. Text reveals follow the VO word by word.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on its word.

Expected transcript:
> These were spaces like electric vehicles [0.0–1.2], drone technology [1.9–2.1], digital payments [2.8–3.0], 5G [3.7] and renewable energy [4.1–4.7].

## Beats — dark background
A collage of desaturated (~70% grey) b-roll tiles builds up around the centre. Each tile carries a white Bold Italic label (~20 px) at one corner. Each tile pops in on its word (scale 0.9 → 1.0, quick fade) and the collage re-centres smoothly as it grows:
1. **"electric vehicles":** a tile (~160 x 120) of EV assembly robots, first alone at the centre, then shifted up-left. Label "Electrical Vehicles" above it.
2. **"drone technology":** a tile (~160 x 160) of a person flying a drone, placed below-right. Label "Drone Technology" below it.
3. **"digital payments":** a tile (~100 x 100) of a phone scanning a QR code at a shop, at the top-right. Label "Digital Payments" beside it.
4. **"5G":** a tile (~100 x 100) of a 5G tower, below-left. Label "5G" beside it.
5. **"renewable energy":** a tile (~100 x 90) of rows of solar panels, at the far left. Label "Renewable Energy" above it.

Hold with a slow drift.

## Sound
A soft click-pop for each tile, a subtle tech whoosh, and a low ambient pad.

## Images — the only thing you may ask about
Before building, send one short message listing short clips of EV assembly robots, a drone flight, QR-code payment, a 5G tower and solar panels, plus the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
