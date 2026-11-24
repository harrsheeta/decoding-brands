# PROMPT 38 — How Why What Columns (How_why_what_graphic, 13.3 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (How_why_what_graphic audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `How_why_what_graphic_4K_sfx.mp4` (sound effects only) and `How_why_what_graphic_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~13.3 s).

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

Expected transcript (it starts mid-word):
> …today's episode, I will talk about exactly how this paparazzi economy works [0.0–4.0], why celebrities are actually paying photographers to follow them [4.8–7.9], and what all of this really means for how people like you and I really consume content [8.1–12.6].

## Look
Dark background. Three equal columns across the frame (~300 px each, starting at x ≈ 36), with a thin dotted horizontal guide line above and below the image row.
- **Top row:** three black & white image panels (~300 x 160 px). A small white dot node sits at each panel's bottom-left corner on the guide line.
  1. A crowd of photographers with cameras
  2. A celebrity at a press wall / step-and-repeat banner
  3. A hand scrolling a phone
- **Under each panel:** a big word in Bold (~52 px), "HOW", "WHY", "WHAT", and a two-line question in Regular (~22 px):
  - "this paparazzi economy works?"
  - "celebrities are paying to photographers?"
  - "this means for how we consume content?"
- **Inactive columns:** the word in sage (#8CB5A3), the question in grey, the photo dimmed.
- **Active column:** a vertical deep-green gradient band (#2F6B55 at the top → transparent at the bottom) fills the whole column behind the photo and text. The word turns white, the question turns white, the photo brightens, and its dot node grows slightly.

## Motion
- **0.0 → ~2.4 s:** the panels wipe in left → right, and each word types in letter by letter with its question fading after: HOW on "how", WHY as the line continues, WHAT just after. All three are visible by ~2.4 s.
- **On "how this paparazzi economy works":** the green band appears on HOW.
- **On "why":** the band slides to WHY (ease-in-out, 0.4 s). The WHY photo cycles through 3 celebrity paparazzi shots (cross-fades ~1 s each).
- **On "what":** the band slides to WHAT. The WHAT photo cycles through phone-scrolling shots (a hand with phone, a feed on screen). Hold.

## Sound
A soft typing tick for the words, a smooth "slide" swoosh each time the band moves, quiet camera shutter clicks under the WHY photos, and a phone scroll tick under WHAT. Low ambient pad.

## Images — the only thing you may ask about
Before building, send one short message listing (1) a photo of a crowd of photographers, (2) 3 celebrity paparazzi / press-wall photos, (3) 2–3 phone-scrolling photos, (4) the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
