# PROMPT 33 — Political Product Controversial Feed (text_based_graphics, 5.6 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (text_based_graphics audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `text_based_graphics_4K_sfx.mp4` (sound effects only) and `text_based_graphics_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~5.6 s).

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
> …endorsing a political party [0.0–1.2], or promoting a problematic product [1.4–3.4], or saying something controversial [3.6–5.4].

## Layout
Three beats in a vertical "feed". Each beat is one tall photo card (~375 x 470 px, square corners, soft shadow) plus a two-line text block beside it. The photo side alternates. Between beats the whole layout scrolls upward (ease-in-out, ~0.4 s): the old card leaves through the top and the new card rises from the bottom.

## Beats
1. **"Endorsing a political party" (0.0 → ~1.3 s).** Photo on the LEFT: a smiling Indian politician in a white kurta waving at a rally, with a blurred saffron/teal Hindi banner behind him. Text on the right, left-aligned: "Endorsing a" (Regular, ~40 px) over "**political party**" (Bold, ~60 px). The words light up with the VO.
2. **"Promoting a problematic product" (~1.4 → ~3.5 s).** Scroll up. Photo on the RIGHT: a smiling man in a tweed blazer holding up a dark product box, with golden backlight. Text on the left: "Promoting a" over "**problematic product**" (Bold, two lines).
3. **"Saying something controversial" (~3.6 → end).** Scroll up. Photo on the LEFT: a man in profile speaking into a cluster of press microphones, moody blue-grey backlight and bokeh. Text on the right: "Saying something" over "**controversial**", revealed letter by letter on the word. Hold.

## Sound
A soft "swipe" whoosh on each scroll, a subtle tick as each bold line lands, and a low ambient pad.

## Images — the only thing you may ask about
Before building, send one short message listing the three photos above plus the two watermark logos (Zero01 Network, Decoding Brands) and ask whether I'll upload them or you should source or create them. The people should be generic, not real identifiable people. If I don't reply, create or source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
