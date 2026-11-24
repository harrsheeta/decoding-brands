# PROMPT 63 — iPhone 600 vs 8 Nike 100 vs 2 5 (ui_animation_with_brolls, 15.5 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (ui_animation_with_brolls audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `ui_animation_with_brolls_4K_sfx.mp4` (sound effects only) and `ui_animation_with_brolls_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~15.5 s).

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
> [When] Apple sells an iPhone, they take home around $600 in profit [0.0–3.5], but the Chinese factory that assembles these iPhones earns only roughly about $8 [4.2–7.9]. Very similarly, if a Nike sneaker sells for $100 [8.7–11.4], the factory that makes it only earns about $2.5 [12.2–15.1].

## Look — macOS desktop
The background is the El Capitan sunset-mountain wallpaper (no dock or menu clutter). UI windows are macOS Safari-style: a light title bar with traffic-light dots and a URL field, soft shadows.

## Beats
1. **0.0 → ~1.3 s:** a Safari window of the Apple "Buy iPhone 12" page (blue iPhone 12, model options) slides in right of centre and then collapses into a white rounded product tile (~180 x 170 px) holding just the blue iPhone 12.
2. **"they take home around $600 in profit" (~1.5 → ~3.6 s):** the tile moves left. A small Apple logo and a grey italic label tab "Profit per unit" appear above it. On "$600", a navy box (#1C2E5A) with "**$600**" (white Bold Italic, ~44 px) pops in to its right.
3. **"Chinese factory … earns only roughly about $8" (~4.2 → ~8.4 s):** the iPhone group swipes off left, and a new tile slides in: footage of a Chinese factory worker assembling electronics, with a small China flag and an "Earns around" label tab. On "$8", a red box (#D7262B) with "**$8**" pops in.
4. **"Nike sneaker sells for $100" (~8.7 → ~11.6 s):** a Safari window of the Nike "Air Jordan 1 — Men's Shoes — $100" product page flies in and the camera zooms into the price area. Then the window slides left and a white tile with the Air Jordan 1 shoe (white/mauve) appears.
5. **"factory … only earns about $2.5" (~12.2 → end):** a scanned Chinese invoice (fapiao) document with a Nike logo slides in at the left. A red hand-drawn circle loops around its stamp area, and "**$2.5 / Unit**" in red appears on it. Hold.

## Sound
A soft UI click and window whoosh for each window, a "ka-ching" for $600, a low dull thud for $8, a sneaker squeak for the Nike tile, and a paper slide plus marker circle swish for the invoice.

## Images — the only thing you may ask about
Before building, send one short message listing (1) an El Capitan wallpaper, (2) an Apple iPhone 12 buy page and an iPhone 12 image, (3) a factory-worker clip, (4) a Nike Air Jordan 1 product page and shoe image, (5) a Chinese invoice image with a Nike logo, (6) the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source or create them. If I don't reply, source or create them yourself (UI pages can be rebuilt in HTML).

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
