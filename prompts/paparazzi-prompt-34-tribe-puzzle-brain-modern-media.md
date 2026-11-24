# PROMPT 34 — Tribe Puzzle Brain Modern Media (puzzle_motion_graphics, 12.5 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (puzzle_motion_graphics audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `puzzle_motion_graphics_4K_sfx.mp4` (sound effects only) and `puzzle_motion_graphics_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~12.5 s).

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
> …somebody regularly, you naturally start treating them like they are a part of your community [0.0–4.6] or your tribe [4.7–5.2]. But our brains [6.0–6.3] have not yet fully adapted [6.5–7.4] to modern media [8.0–8.6], which is where we get to see people [9.4–10.6] without really knowing them personally [11.0–12.3].

## Scene 1 — the tribe puzzle (0.0 → ~5.9 s)
- Dark background scattered with ~25 soft 3D jigsaw pieces in grey (glossy grey gradient, subtle bevel and shadow), at random angles and sizes. They drift and rotate slowly with gentle depth parallax, and the camera rotates slowly (~8° over the scene).
- On "start treating": ONE piece in the centre turns warm orange (#E8962F, with a deep red #B3201F gradient glow on one edge) and moves forward.
- From "like they are a part of your community" onward: more orange pieces fly in from the grey crowd and snap into it one by one (each with a small click and settle) until they form a locked 3x3 cluster by "tribe". The red glow shifts inside the cluster like warmth.

## Scene 2 — the brain (~6.0 → ~8.0 s)
- Hard cut to a layout grid: thin grey lines (#3A3A3A) divide the frame into panels.
- On "our brains": a sagittal brain MRI image in a red-orange "hot" colour map sits in the centre panel, filling it.
- On "not yet fully adapted": the brain shrinks to a smaller centre panel. Above it, "Not Yet Fully Adapted" (Medium, ~44 px, white) appears with a random-character decode scramble (~0.4 s).

## Scene 3 — modern media (~8.0 → end)
- On "modern media": the brain is replaced by a wide collage of black & white paparazzi/street photos (celebrities walking, crowds, cameras), a grid of 12–15 tiles inside a wide panel. "**Modern Media**" (Bold, ~72 px, white) decodes in over the collage's left part.
- On "which is where we get to see people": the collage slowly expands and pans right. The grid lines slide to new positions.
- On "without really knowing them personally": the title block shifts left and settles. Hold.

## Sound
A soft ambient pad. A light plastic click for each puzzle piece snapping in, and a warm swell as the cluster completes. A hard cut "thump" into the brain. A digital decode chatter for each scrambled title. A camera-shutter flurry under the collage.

## Images — the only thing you may ask about
Before building, send one short message listing (1) a sagittal brain MRI in a hot colour map, (2) 12–15 black & white paparazzi/street photos, (3) the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. The puzzle pieces are drawn in code. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
