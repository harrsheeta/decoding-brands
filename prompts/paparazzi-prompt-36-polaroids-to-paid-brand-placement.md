# PROMPT 36 — Polaroids To Paid Brand Placement (motion_graphics, 13.4 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (motion_graphics audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `motion_graphics_4K_sfx.mp4` (sound effects only) and `motion_graphics_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~13.4 s).

## Show look — "Decoding Brands" (Zero01 Network)
This is my Decoding Brands episode on the paparazzi economy. Ignore my saved Jet Airways / Meta / idk / dairy themes and any saved article rules; follow ONLY this look.
- **Watermarks on every frame:**
  - top-left: the "ZERO01⚡NETWORK" logo (white bold italic, small, ~22 px tall, 30 px from the edges)
  - top-right: the "DECODING BRANDS" badge (yellow-green speech-bubble sticker, ~60 px)
- **Background:** dark charcoal (#1E1E1E centre → #0C0C0C edges), with soft large blurred light blobs drifting very slowly and a soft vignette.
- **Type:** Neue Haas Grotesk / Helvetica Neue (fallback Inter), tight letter-spacing (−2%). Headlines Medium/Bold, body Regular.
  - Text colours: white #F5F5F5, or soft cream #F1EFC6 for "concept" words.
  - Accents: deep green #1F5A44 and sage #8CB5A3.
- **Photos:** warm, cinematic, slightly desaturated, with soft shadows. Archive and paparazzi photos are often black & white.
- **Text reveals:** follow the VO word by word. Each word fades from ~25% grey to full colour as it's spoken. Some reveals use a quick random-character "decode" scramble (noted per scene).
- **Motion:** smooth, eased (ease-out quint), with gentle continuous camera drift. Nothing static.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on its word.

Expected transcript (it starts mid-sentence):
> …favourites that you spot your favourite celebrities wearing [0.0–1.7], they are actually organized specifically for this purpose [2.4–5.1]. Those accessories [5.9–6.0], sunglasses [6.9] and sometimes even the coffee cups that they are holding [7.8–9.7], all of it could potentially be a paid brand placement [10.3–12.9].

## Scene 1 — the polaroids (0.0 → ~5.2 s)
- On a dark background, colour paparazzi photos of celebrities (airport and street looks, with sunglasses, bags and coffee) are tossed in one by one as white-bordered polaroids. Each enters from a random edge, rotated, with a small bounce and shadow, landing scattered across the frame. About 5 by 1.7 s.
- On "organized": all polaroids desaturate to black & white at once.
- On "specifically for this purpose": they straighten up and slide into a neat, slightly overlapping collage on the left third (2 columns).

## Scene 2 — the items (~5.2 → ~10.3 s)
- A thin vertical divider line draws down the frame at x ≈ 30%, with the collage to its left.
- On the right, a horizontal carousel of rounded dark-grey tiles (~110 px, soft 3D shading). Each holds a semi-realistic object icon with a small grey label under it.
- The carousel slides left so each item comes to the centre on its word:
  - a handbag, "Accessories"
  - black sunglasses, "Sunglasses"
  - a white coffee cup with a green sleeve, "Coffee cups"

## Scene 3 — paid brand placement (~10.3 → end)
- On "all of it": the collage and divider slide off left, and the three tiles line up centred in a row.
- On "paid brand placement": "**Paid Brand** Placement" appears centred below the tiles ("Paid Brand" Bold, "Placement" Regular, ~40 px), word by word with a slight upward slide.
- Soft light blobs drift behind. Hold.

## Sound
A paper/photo flick for each polaroid landing, a camera shutter click on the desaturate, and a soft "shuffle" as they organize. A UI tick for each tile, and a confident low "ding" on "paid brand placement".

## Images — the only thing you may ask about
Before building, send one short message listing (1) 5 paparazzi photos of celebrities in airport/street looks, (2) 3D-ish icons of a handbag, sunglasses and a coffee cup with a green sleeve (or I can have you draw them), (3) the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source or create them. If I don't reply, create the icons and use generic street-style photos.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
