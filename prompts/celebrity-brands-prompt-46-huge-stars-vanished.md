# PROMPT 46 — Huge Stars Vanished (tiles_and_text_animations, 8.0 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (tiles_and_text_animations audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `tiles_and_text_animations_4K_sfx.mp4` (sound effects only) and `tiles_and_text_animations_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~8.0 s).

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

Expected transcript (it starts mid-list):
> …and Preity Zinta [0.2–0.7], Govinda [1.1], Bipasha Basu [1.7–2.1], etc. [2.3] They were all huge stars at one point in time [3.1–5.2]. But today [5.7–5.8], they have practically vanished from the entire universe [6.2–7.8].

## Look and beats
- Dark background with a soft centre glow and a strong vignette.
- A single horizontal row of video tiles (~150 x 200 px each, no gaps, square corners) builds from the left, starting at x ≈ 70. Each tile plays a short film clip of that star.
  - **0.0 s:** tile 1 (the previous name, a male star) is already there.
  - Preity Zinta's tile slides in on "Preity Zinta", Govinda's on "Govinda", Bipasha Basu's on "Bipasha Basu".
- **"They were all":** small white Regular text (~20 px) above the row's top-left.
- **"huge stars":** "**Huge Stars**" in Bold Italic (~40 px, white) under the row's bottom-right, revealed word by word.
- **"But today":** the tiles disappear one by one from the left (each snaps to black). By "vanished", the text and all tiles are gone.
- **On "vanished":** "**Vanished**" (Bold, ~60 px, white) fades in centred, then slowly fades and blurs slightly to the end.

## Sound
A soft film-projector click as each tile appears, a whoosh-swell under "Huge Stars", a sharp "cut" click for each tile vanishing, then an airy reverse-reverb swell on "Vanished".

## Images — the only thing you may ask about
Before building, send one short message listing short film clips (or stills) of the four stars (the first tile's star, Preity Zinta, Govinda, Bipasha Basu) plus the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
