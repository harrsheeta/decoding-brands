# PROMPT 49 — Film Fee Tile Wall 40cr to 10cr (Tile_animation_with_text, 12.5 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (Tile_animation_with_text audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `Tile_animation_with_text_4K_sfx.mp4` (sound effects only) and `Tile_animation_with_text_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~12.5 s).

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
> See, if you are doing about two films a year at, let's say, 20 crore rupees each [0.0–3.1], that is about 40 crore rupees [3.7–5.2]. But after taxes [5.4–5.8], manager fees [6.6–6.8] and other expenses [7.2–7.7], you are left with approximately half of it [8.6–10.4], which in this case happens to be 10 crore [10.5–12.2].

## Look
- Black background with a soft vignette.
- Film footage is shown inside a "tile wall": the footage is cut by thin black grid lines into ~6 x 3 tiles per row, so it looks like a video wall. Two rows stacked (two films), each ~980 x 260 px, centred.
- Numbers are big, very widely spaced, white Bold with a slight bevel/shadow (~64 px): "2 0 C R".

## Beats
1. **"two films a year" (0.0 → ~2.2 s):** the two rows of tiles fill in with film footage (top: a desert action scene with birds; bottom: the hero in a red scarf), with a quick random flicker of tiles turning on.
2. **"20 crore rupees each" (~2.2 → ~3.6 s):** the footage darkens to ~40%. "2 0 C R" appears over the top row, then over the bottom row.
3. **"about 40 crore rupees" (~3.7 → ~5.3 s):** the two numbers slide together and merge into one centred "4 0 C R". The rows dim further.
4. **"after taxes, manager fees and other expenses" (~5.4 → ~8.5 s):** the number fades out and new action footage plays in the wall. On each of "taxes", "manager fees" and "other expenses", a column (or two) of tiles snaps off from the edges, so the wall shrinks narrower each time (~980 → ~720 → ~500 → ~300 px wide), staying centred.
5. **"left with approximately half" (~8.6 → ~10.4 s):** the wall keeps cycling footage at its smaller size.
6. **"10 crore" (~10.5 → end):** the footage darkens, and "1 0 C R" appears centred over the small wall. Hold.

## Sound
A projector whir under the footage, a cash "ka-ching" for each 20 CR and a heavier one for 40 CR, a crisp "snip"/glass-tap as each column of tiles drops off, and a low thud on 10 CR.

## Images — the only thing you may ask about
Before building, send one short message listing short action-film clips (two different films, several shots each) and the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, use generic cinematic action footage.

## Note
Keep the VO's numbers: 20 CR each → 40 CR → 10 CR.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
