# PROMPT 57 — Xiaomi 2014 India (broll_ideas_with_year, 8.7 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (broll_ideas_with_year audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `broll_ideas_with_year_4K_sfx.mp4` (sound effects only) and `broll_ideas_with_year_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~8.7 s).

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
> In 2014 [0.0–0.6], when Xiaomi entered India [0.8–1.7], they did not just translate their Chinese playbook exactly into India [2.3–5.1], they actually completely rewrote it, customized to India [5.7–8.3].

## Beats — dark background
1. **"In 2014" (0.0 → ~0.8 s):** four big bevelled grey tiles in a row, centred (~95 x 95 px each, silver gradient with an inner shadow), holding "2", "0", "1", "4" in white Bold Italic. At first the "0" tile plays a short clip of the Mumbai skyline instead of a digit; on "2014" it flips to "0".
2. **"Xiaomi entered India" (~0.8 → ~2.2 s):** the tiles fly apart and a white-bordered video card (~540 x 200 px) plays a hand holding a Xiaomi/Redmi phone outdoors, with a park behind.
3. **"did not just translate their Chinese playbook" (~2.3 → ~5.6 s):** fast, angled product close-ups in a wide white-background card: a red Redmi phone's back, its camera bump, then the blue-to-purple gradient screen of a Redmi Note 7. Crops slide diagonally with each cut (~0.7 s each).
4. **"completely rewrote it, customized to India" (~5.7 → end):** a dynamic collage of b-roll tiles assembles: a Snapdragon chip render, a phone fast-charging, gaming on a phone, a crowd of Indian buyers, phone cameras. It settles into one big centre tile (the hand holding the phone) with smaller tiles at both sides. Hold.

## Sound
A slot-tile "clack" for each digit, a whoosh for each layout change, quick product "swish" hits for the close-ups, and an upbeat pulse under the collage.

## Images — the only thing you may ask about
Before building, send one short message listing (1) a Mumbai skyline clip, (2) Xiaomi/Redmi phone product shots and in-hand clips, (3) a Snapdragon chip render and clips of charging, gaming and Indian crowds, (4) the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
