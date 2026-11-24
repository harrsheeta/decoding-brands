# PROMPT 51 — 82E vs Hyphen Revenue Bars (Graph_animation, 12.1 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (Graph_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `Graph_animation_4K_sfx.mp4` (sound effects only) and `Graph_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~12.1 s).

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

Expected transcript (Whisper hears "82°E" as "82 million"):
> …82°E by Deepika Padukone had revenues of 23 crore rupees in FY 2024 [0.0–4.4] and it was loss making [5.0–6.4]. [Hyphen by Kriti Sanon] has already crossed 100 crore rupees in revenue [7.0–9.7] and it has relatively lower losses [10.4–11.6].

## Look
- Dark background with a vignette.
- A bar chart drawn in thin white lines with a faint grid:
  - Y axis "Amount in ₹ Crore", 0–100 in steps of 20.
  - X axis labels: "82°E" (with "Deepika Padukone" small under it) and the "HYPHEN" wordmark (with "Kriti Sanon" under it).
- Title above the chart: "*Revenue of*" (small Italic cream) over "**BRANDS IN FY2024**" (Bold condensed, white).
- Bars: deep green with a top-to-bottom gradient (#2E6E57 → #1C3F33) and a white Bold condensed value inside near the top ("23CR"). A loss-making bar turns into a maroon gradient (#8E1B22 → transparent).

## Beats
1. **0.0 → ~1.0 s:** axis arrows draw from the origin with tick numbers. The camera starts close and tilted, like looking along a 3D floor.
2. **"82°E by Deepika Padukone" (~1.0 → ~2.2 s):** the grid lays out in 3D perspective and the 82°E label appears.
3. **"revenues of 23 crore rupees" (~2.2 → ~3.8 s):** the 82°E bar rises while its value counts 0 → 23CR.
4. **"in FY 2024" (~4.0 s):** the camera eases into a flat 2D front view and the title types in.
5. **"it was loss making" (~5.0 → ~6.5 s):** "*Loss Making*" (small Italic) appears above the bar, and the bar turns maroon.
6. **"has already crossed 100 crore" (~7.0 → ~9.8 s):** the camera dives in close to the Hyphen slot. Its green bar rises, filling the frame, while the value counts 20 → 65 → 98 → 100CR.
7. **"relatively lower losses" (~10.0 → end):** the camera pulls back to the full flat chart, and the Hyphen bar also turns to a maroon gradient (loss-making, but a smaller loss). Hold.

## Sound
A drawing "zip" for the axes, a rising tone with each bar, counter ticks, a low dull thud when a bar turns maroon, and a whoosh for each camera move.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the 82°E and HYPHEN logos plus the Zero01 Network / Decoding Brands logos, or you should source them. If I don't reply, source them yourself.

## Note
This clip starts mid-sentence. The Hyphen bar appears even though "Hyphen by Kriti Sanon" falls in the part of the VO that's cut off. Keep the figures: 82°E 23 CR (loss-making), Hyphen 100 CR.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
