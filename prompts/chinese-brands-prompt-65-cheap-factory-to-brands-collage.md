# PROMPT 65 — Cheap Factory to Brands Collage (broll_ideas, 6.4 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (broll_ideas audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `broll_ideas_4K_sfx.mp4` (sound effects only) and `broll_ideas_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~6.4 s).

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

Expected transcript (it starts mid-sentence):
> …as the world's cheap factory [0.0–1.3] to now creating brands that global consumers actually want [1.7–4.4] and aspire to own? [4.9–5.8]

## Beats — black background
- Behind everything: a huge dark-red "CHINA" (#3B0E0E, ~420 px, Bold, ~60% opacity), centred and partly covered by the collage.
1. **"world's cheap factory" (0.0 → ~1.6 s):** a collage of photo/b-roll tiles stacks up quickly in the centre, each popping in slightly rotated then straightening, with soft shadows:
   - an old Chinese postage stamp (orange, vintage)
   - a plain grey factory building
   - an aerial shot of blue-roofed factories
   - a small workshop
2. **"now creating brands" (~1.7 → ~4.6 s):** modern brand b-roll stacks over the old tiles, larger and glossier, ~0.6 s apart:
   - a BYD EV driving (blue-grey car)
   - a Li-Ning racket ad ("dynamic optimum frame")
   - a Lenovo laptop ad ("Re-engineered for longevity")
   - a glass building detail
   The old tiles slide down-left as the new ones take the top-right.
3. **"and aspire to own" (~4.9 s → end):** hard cut to a grey low-poly 3D globe/map (light grey landmasses on dark grey) slowly rotating toward Asia. Hold.

## Sound
A stamp/paper flick for the old tiles, sleek "swoosh-whoosh" hits for the modern tiles, and a deep airy swell on the globe cut.

## Images — the only thing you may ask about
Before building, send one short message listing (1) old-China tiles (vintage stamp, factory buildings, an aerial factory shot), (2) modern brand clips (BYD car, Li-Ning racket ad, Lenovo laptop ad), (3) the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source them. Draw the globe in code. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
