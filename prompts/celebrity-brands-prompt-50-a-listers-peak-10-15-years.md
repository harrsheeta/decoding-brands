# PROMPT 50 — A Listers Peak 10 15 Years (Motion_graphics_and_text_animation, 5.5 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (Motion_graphics_and_text_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `Motion_graphics_and_text_animation_4K_sfx.mp4` (sound effects only) and `Motion_graphics_and_text_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~5.5 s).

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
> See, a typical Bollywood A-lister's earning window [0.0–2.2] might be at the peak for about 10–15 years at best [2.5–5.3].

## Beats
1. **"typical Bollywood A-lister" (0.0 → ~2.4 s):** a row of portrait tiles (~150 x 200 px, small gaps) of top Bollywood stars slides slowly right-to-left across a dark background with a soft vignette. Order: Salman Khan, Hrithik Roshan, Akshay Kumar, Aamir Khan, Ranbir Kapoor, Shah Rukh Khan. New tiles enter from the right as old ones leave left.
2. **"might be at the peak" (~2.5 → ~3.6 s):** the row keeps moving, then the last tile (Shah Rukh Khan) grows into a tall full-length portrait (~150 x 300 px, dark suit) and rises above the row. The other tiles slide down and partly out of the bottom-left.
3. **"10–15 years at best" (~3.6 → end):** to the right of the tall tile's top: "**10-15**" (Bold, ~34 px) with "yrs" (small Italic grey), then "at **best**" in Bold Italic below, revealed word by word. Hold, with a slow drift.

## Sound
A smooth slide whoosh under the moving row, a soft rising "lift" swell as the tall tile rises, and a tick for each text word.

## Images — the only thing you may ask about
Before building, send one short message listing portrait photos of Salman Khan, Hrithik Roshan, Akshay Kumar, Aamir Khan, Ranbir Kapoor and a full-length Shah Rukh Khan, plus the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
