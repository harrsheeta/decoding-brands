# PROMPT 48 — Timeline 20cr to 2cr (Timeline_animation, 5.9 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (Timeline_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `Timeline_animation_4K_sfx.mp4` (sound effects only) and `Timeline_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~5.9 s).

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

Expected transcript (it ends mid-word):
> If you fast forward 10 years [0.0–1.0], those 20 crore rupees offers [1.5–2.5] drop to 2 crore rupees [2.7–4.3], just because you are no longer re[levant]… [4.3–5.7]

## Beats
1. **Fast forward (0.0 → ~1.4 s):** a horizontal timeline of year cells across the middle (each ~150 x 160 px, dark grey, divided by thin vertical lines, with a soft spotlight on the centre cell). Years in white Bold Italic (~32 px).
   - It scrolls quickly left from 2017 to 2026, decelerating, and stops with 2024 / 2025 / 2026 centred.
   - Then 2025 dims to grey.
2. **"those 20 crore rupees offers" (~1.4 → ~2.6 s):** a square photo card (~210 px) drops into the 2025 slot with a little tilt: a young star smiling, with confetti around him. "**20cr.**" in Bold Italic white (~40 px) sits over it.
3. **"drop to 2 crore" (~2.7 → ~4.3 s):** the card tilts and drops slightly. The timeline fades away to a plain dark-grey background with a vignette. The card's photo changes to the same person, older, sitting alone at a bar in dim amber light, and the text changes to "**2cr.**".
4. **"just because you are no longer relevant" (~4.3 → end):** "Just / because / you are" (white Regular, ~24 px, right-aligned) appears line by line at the card's top-left. Then "no longer" (Regular) and "**Relevant**" (Bold Italic, gold #C9B487) at its bottom-right. Hold.

## Sound
A fast reel-scroll whir that ticks as it slows, a celebratory confetti pop with the 20cr. card, then a downward "deflate" whoosh and low thud on the drop to 2cr. A sombre low pad at the end.

## Images — the only thing you may ask about
Before building, send one short message listing (1) a photo of a young actor smiling with confetti, (2) the same type of actor (or a lookalike) older, sitting alone at a dim bar, (3) the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source or create them. If I don't reply, source or create them yourself (generic, not a real identifiable person).

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
