# PROMPT 61 — Worlds Factory to Worlds Brand (dynamic_broll, 2.4 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (dynamic_broll audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `dynamic_broll_4K_sfx.mp4` (sound effects only) and `dynamic_broll_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~2.4 s).

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

Expected transcript (it ends mid-sentence):
> …turn China from the world's factory [0.0–1.3] to the world's [brand]… [1.5–2.4]

## Beats — cream background
1. **0.0 → ~0.5 s:** a green-bordered rounded video card (~620 x 400 px) slides in from the right and settles right of centre. It shows Chinese factory workers in blue caps and white uniforms at an assembly line.
2. **On "world's factory" (~0.5 s):** left of the card, a small black italic "World's" sits over a big green condensed "**FACTORY**" (~60 px), revealed word by word.
3. **On "to the world's" (~1.6 s):** a quick swap. The card slides to the left side and its footage changes to Xi Jinping giving an address (Chinese flag behind him, "中国 CHINA" name card). The text moves to the right and reads "*World's* / **BRAND**". Hold.

## Sound
A card slide whoosh, factory machine ambience under the first card, a quick swap swish, and a firm low accent on "BRAND".

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload (1) the factory-worker clip, (2) the Xi Jinping address clip, and (3) the Zero01 / Decoding Brands logos, or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
