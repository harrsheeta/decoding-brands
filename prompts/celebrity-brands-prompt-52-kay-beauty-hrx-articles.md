# PROMPT 52 — Kay Beauty HRX Articles (article_animation, 10.3 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (article_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `article_animation_4K_sfx.mp4` (sound effects only) and `article_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~10.3 s).

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

Expected transcript (Whisper mishears "Hrithik Roshan"):
> K-Beauty, for example [0.0–0.7], made 88 crore rupees in revenue last year [1.4–3.6] with an 11 crore profit [3.9–5.3], and HRX by Hrithik Roshan [6.1–7.0] crossed 1000 crore rupees in revenue last year [7.4–10.0].

## Note
This overrides my saved "article animation" rules. Follow exactly what's below.

## Article 1 — Storyboard18, dark (0.0 → ~5.4 s)
- **Background:** a darkened, blurred photo of Katrina Kaif (~25% brightness) with a soft vignette.
- **Article:** no card, just text over the photo, left-aligned at x ≈ 70:
  - small grey caps "STORYBOARD18" with a thin rule under it
  - headline in white Bold (~30 px): "Katrina Kaif's Kay Beauty made ₹88 crore revenue and ₹11 crore profit in FY 2024"
  - body in light grey (~16 px): "Kay Beauty, launched in 2019 by Katrina Kaif with Nykaa, earned ₹88.23 crore in revenue and ₹11.3 crore profit in FY 2024, marking its third profitable year. Its affordable pricing around ₹299 and focus on everyday needs helped it stand out in India's competitive beauty market. The brand is now expanding internationally and setting a benchmark for celebrity-backed beauty lines."
  - "By Mansi Jaswal · Dec 30, 2024"
- **Motion:**
  - 0.0–1.4 s: the headline types in word by word.
  - On "88 crore": the camera zooms in (~2.2x) and "₹88 crore" gets an inverted highlight (a white box behind it, black text) that snaps on.
  - On "11 crore profit": a fast horizontal whip-blur pan, then "₹11 crore" gets the same white box.
  - ~5.0 s: pull back to the full article.

## Article 2 — Hindustan Times, light (~5.5 → end)
- **Transition:** a hard cut with a quick flash to a light cream (#FBF6EA) news page in Hindustan Times style.
- **Page content:**
  - a small top bar with the masthead "Hindustan Times" centred
  - a "Brands" kicker
  - headline in black Bold (~26 px): "Hrithik Roshan's HRX is a ₹1000-crore juggernaut: Celebrity-led brands' report card"
  - standfirst: "A recent analysis of celeb-led brands has revealed that only a handful of them are turning profit and not struggling to stay afloat."
  - a hero image area that cycles through 3–4 HRX campaign stills of Hrithik Roshan, crossfading every ~1 s
- **Motion:** slow drift down the page. On "1000 crore": "₹1000-crore" in the headline gets an inverted highlight (a black box, white text). Hold.

## Sound
Soft keyboard ticks for the typing headline, a marker "snap" on each highlight, a whip whoosh, a page flash "swish" into Article 2, and a light newsroom ambience.

## Images — the only thing you may ask about
Before building, send one short message listing (1) a Katrina Kaif photo for the background, (2) 3–4 HRX campaign stills of Hrithik Roshan, (3) the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself. Use the real Storyboard18 and Hindustan Times article text if you can find it; otherwise use the text above exactly.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
