# PROMPT 47 — Earnings Rise vs Decline Curves (graph_animation_1, 7.2 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (graph_animation_1 audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `graph_animation_1_4K_sfx.mp4` (sound effects only) and `graph_animation_1_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~7.2 s).

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
> All of a sudden [0.0–0.4], instead of your earnings increasing as your career progresses [0.9–3.2], your annual income starts declining very quickly [4.1–6.4].

## Look
- Dark background with a faint large grid (~#1A1A1A lines, ~200 px) and a soft centre glow.
- Captions: Regular white words with key words in Bold Italic cream (#F1EFC6), revealed word by word on the VO.

## Beats
1. **0.0 → ~4.0 s:** an orange-pink dashed curve (#F08A6B, ~3 px, dashes 8/6) draws from the bottom-left in a rising exponential. The camera follows its tip up and to the right.
   - At the tip, a white dashed vertical drop line and a horizontal guide appear (crosshair).
   - To the right of the vertical line, the caption: "instead of **earning increasing** as the career progresses".
2. **~4.0 → ~6.4 s:** cut. The camera is now lower. A solid teal curve (#6FD3B5, ~3 px, soft glow) draws from the top-left downward, flattening toward the bottom (exponential decline).
   - Caption: "Annual income starts **declining very quickly**".
3. **~6.4 → end:** the camera pulls back so both curves cross in the frame (an X). Both captions stay, smaller, beside their curves. Hold.

## Sound
A soft rising synth tone with the orange curve, a hard-cut whoosh, a descending tone with the teal curve, a gentle low hit when the view pulls back, and ticks for the text.

## Images
Draw everything in code. This clip needs no outside images, so don't ask me anything; just build it. Use the Zero01 Network and Decoding Brands logos if they're in your files, otherwise recreate them as simple text/badge marks.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
