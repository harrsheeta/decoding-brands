# PROMPT 54 — Celebrity Brand Logo Reveal (Logo_reveal_animation, 4.2 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (Logo_reveal_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `Logo_reveal_animation_4K_sfx.mp4` (sound effects only) and `Logo_reveal_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~4.2 s).

## Show look — "Decoding Brands" (Zero01 Network)
This is my Decoding Brands episode on celebrity-owned brands. Ignore my saved Jet Airways / Meta / idk / dairy themes and any saved article rules; follow ONLY this look.
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

Expected transcript:
> Mind you, these were not small experiments [0.0–1.4] that celebrities were trying on the side [2.0–3.5].

## Look
- Dark background with a subtle fine hex-mesh texture and a soft centre glow.
- Tiles: black squares/rectangles with thin grey-green borders (#3C4A44), each holding a white brand logo.
- The tiles lock together into a tight, staggered centred cluster (a honeycomb-like offset brick pattern, ~420 x 300 px overall).

Brands (logo → the celebrity who owns it):
- RHESON → Sonam Kapoor
- JUSTF → Jacqueline Fernandez
- NUSH → Anushka Sharma
- 82°E → Deepika Padukone
- YWC (YouWeCan) → Yuvraj Singh
- SKULT → Shahid Kapoor

## Beats
1. **"Mind you, these were not small experiments" (0.0 → ~1.6 s):** the tiles fly in from off-screen in different directions, blurred and out of focus with motion blur, a few empty outlined tiles flicking through. They snap into the cluster one by one, coming into focus (blur → sharp).
2. **"that celebrities" (~2.0 → ~3.0 s):** each logo tile flips (a 3D card flip on the vertical axis, staggered ~0.12 s) to show the owner's head-and-shoulders photo in the same slot.
3. **"on the side" (~3.0 → end):** a final tile settles. The cluster of six celebrity photos holds with a slow push-in.

## Sound
A whoosh for each incoming tile, a soft magnetic "clack" as each locks, a quick card-flip "fwip" for each flip, and a confident low hit when all are revealed.

## Images — the only thing you may ask about
Before building, send one short message listing (1) the six brand logos (RHESON, JUSTF, NUSH, 82°E, YouWeCan, SKULT), (2) the six owners' headshots (Sonam Kapoor, Jacqueline Fernandez, Anushka Sharma, Deepika Padukone, Yuvraj Singh, Shahid Kapoor), (3) the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
