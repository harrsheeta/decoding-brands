# PROMPT 42 — Beauty Brand Price Showcase (Product_and_price_showcase, 12.6 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (Product_and_price_showcase audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `Product_and_price_showcase_4K_sfx.mp4` (sound effects only) and `Product_and_price_showcase_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~12.6 s).

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

Expected transcript (Whisper mishears some brand names and prices; the correct ones are below):
> Forest Essentials at ₹1,000 to ₹3,500 [0.0–2.0], Kama Ayurveda between ₹800 and ₹3,000 [3.1–5.3], The Body Shop between ₹500 and ₹2,500 [6.2–8.2], and Biotique at ₹150 to ₹800 on an average [9.7–12.5].

## Look
For each brand: a collage of 3 overlapping product photos (rectangles of different sizes, soft drop shadows, slightly staggered), the brand name in white Bold (~32 px), and a price range in white Bold (~44 px) with a small regular "to" between the two numbers. Prices reveal word by word (grey → white) on the VO. Between brands, a quick horizontal whip-slide (~0.35 s, light motion blur) moves the whole layout to its next arrangement.

## Beats
1. **Forest Essentials (0.0 → ~3.0 s):** collage at the right half, name above its top-right. On "₹1,000": a soft grey circle (~190 px, #3A3A3A) scales in on the left with "₹1000 / to / ₹3500" stacked inside.
2. **Kama Ayurveda (~3.1 → ~6.1 s):** collage across the middle-right (green oil bottle, product range, pink box). Name top-left over the collage. Price "₹800 to ₹3000" bottom-right.
3. **The Body Shop (~6.2 → ~9.6 s):** collage of 3 in a centred row (the middle one large). Name types in above the centre. Price "₹500 to ₹2500" centred below.
4. **Biotique (~9.7 → end):** collage at the left and centre. Name top-right. Price "₹150 to ₹800" bottom-left. Hold.

## Sound
A whoosh on each whip-slide, a soft tick for each price word, and a subtle cash-register "ding" when each range completes. Low ambient pad.

## Images — the only thing you may ask about
Before building, send one short message listing 3 product photos each for Forest Essentials, Kama Ayurveda, The Body Shop and Biotique, plus the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source real product photos yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
