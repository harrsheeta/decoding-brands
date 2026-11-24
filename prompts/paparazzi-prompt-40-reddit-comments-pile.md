# PROMPT 40 — Reddit Comments Pile (reddit_animation_motion_graphics, 5.6 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (reddit_animation_motion_graphics audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `reddit_animation_motion_graphics_4K_sfx.mp4` (sound effects only) and `reddit_animation_motion_graphics_4K_vo_sfx.mp4` (VO + sound effects).
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

Expected transcript (it ends mid-sentence):
> Now for a few days [0.0–0.6], the entire internet went crazy [0.9–2.6] trying to figure out what these two letters… [3.2–5.1]

## Look
- Background: near-black, with a soft diagonal shaft of white light falling from the top-right toward the bottom-left (a wide, feathered beam). Cards passing through the beam light up brighter.
- Reddit-style comment cards: white, rounded corners (~10 px), soft shadow, ~340 x 150 px at base size. Each card has a round avatar, a bold username, a grey "u/username" handle under it, the red Reddit alien icon at the top-right, the comment text, "1y ago" in small grey, and a row of grey stat icons: comments 487, reposts 56, likes 877, plus a share icon.
- Comment texts (people guessing what "PD" means):

| Username | Comment |
|---|---|
| I-am-Groot_01 | "Pati dev! No need to change it ever!" |
| DONN_2 | "The F is missing" |
| PossessionSecret3195 | "Pandu disha" |
| AwareGiraffe903 | "Pinka Datani" |
| kvak95 | "Duh... it's Piger Droff" |
| the_running_stache | "Pendua Droff" |
| SelmonTheDriver | "Prabhas Darling" |

## Motion
- **0.0 s:** one card (I-am-Groot_01) sits centre-left, small, drifting.
- **From "went crazy" (~0.9 s):** cards pop in one after another (scale 0.85 → 1.0 with a slight overshoot), at varied sizes (0.8x–1.6x) and positions, overlapping into a messy pile. The pace speeds up, and repeats are fine to fill (~12 pops by the end).
- The camera pushes in steadily (1.0 → 1.25) and drifts left, so newer cards are bigger and closer. Hold the clutter to the end.

## Sound
A soft notification "pop" for each card, getting busier, plus a rising murmur of keyboard and typing chatter underneath.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the Reddit icon, avatar images and the Zero01 Network / Decoding Brands logos, or you should create them. Draw the cards in code. If I don't reply, create them yourself (simple cartoon avatars).

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
