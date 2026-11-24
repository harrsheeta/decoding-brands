# PROMPT 56 — Guochao Li Ning PV Sindhu (broll_with_text_ideas, 14.6 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (broll_with_text_ideas audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `broll_with_text_ideas_4K_sfx.mp4` (sound effects only) and `broll_with_text_ideas_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~14.6 s).

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
> Even as a name, it's called Guochao, which means "national tide" in Chinese [0.0–3.7]. Now, a perfect example of this is Chinese sportswear brand Li-Ning [4.0–7.1], which by the way also sponsors India's badminton star PV Sindhu [7.5–10.5]. Now, they got models to walk the ramp in New York wearing jackets with… [11.0–14.6]

## Beats — dark background
1. **0.0 → ~1.4 s:** ~20 small b-roll thumbnails (~90 x 60 px) of modern Chinese pop culture float scattered across the frame with slight parallax: TikTok/Douyin, EVs, sneakers, youth in Chinese-print streetwear, Chinese red packaging.
2. **On "Guochao" (~1.5 s):** "**GUOCHAO**" (white, Helvetica Bold, ~150 px, wide) decodes in at the centre (random-character scramble, ~0.4 s) while the thumbnails shrink into it and vanish. Hold, with a slow push.
3. **~4.0 s:** the word slides down and fades.
4. **On "Li-Ning" (~6.3 s):** the red Li-Ning logo tile (~220 x 110 px) pops in at the centre, with a collage of ~10 Li-Ning b-roll tiles around it (shoes, store, athletes, products) building outward.
5. **On "PV Sindhu" (~8.5 s):** the camera pushes right into the collage, and a large tile (~540 x 300 px) plays footage of PV Sindhu walking onto court at the Paris 2024 Olympics. The logo stays cropped at the left edge.
6. **On "walk the ramp in New York" (~11.0 s):** the layout shifts. A red bar runs across the top, and the main tile plays New York Fashion Week runway footage of models in Li-Ning jackets, with side tiles (a sports bag, a store) cropped at the edges. Hold.

## Sound
Light chatter and swooshes for the floating thumbnails, a digital decode for GUOCHAO, a punchy hit for the Li-Ning logo, arena crowd ambience under PV Sindhu, and a runway beat pulse at the end.

## Images — the only thing you may ask about
Before building, send one short message listing (1) ~20 short Chinese pop-culture b-roll clips, (2) the Li-Ning logo plus ~10 Li-Ning product/athlete clips, (3) PV Sindhu Paris 2024 walk-on footage, (4) Li-Ning New York Fashion Week runway footage, (5) the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
