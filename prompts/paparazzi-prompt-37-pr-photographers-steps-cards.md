# PROMPT 37 — PR Photographers Steps Cards (1_2_3_cards, 10.6 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (1_2_3_cards audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `1_2_3_cards_4K_sfx.mp4` (sound effects only) and `1_2_3_cards_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~10.6 s).

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

Expected transcript:
> PR team calls trusted photographers [0.0–1.8], they tell them exactly when and where to show up [3.0–5.7], and the celebrity then appears looking absolutely perfect [5.8–8.7] for that candid moment [9.2–10.2].

## Look
Dark background with a soft vignette. One wide "ticket" card (~680 x 300 px) sits centred:
- **Left fifth:** a sage panel (#8CB5A3), with a huge step number in a lighter sage (#A9C8BA, ~340 px, condensed bold) cropped by the panel edges.
- **Ticket notch:** a solid deep-green circle (#1F5A44, ~70 px) sits half over the card's left edge, vertically centred.
- **Right four-fifths:** paparazzi video footage with a deep-green duotone tint (~80% #1E4D3B over desaturated footage), playing slowly. Over it, white text, left-aligned:
  - a small line in Regular (~26 px)
  - a big line in condensed bold caps (Bebas Neue Pro, ~44 px)

Cards:
1. "PR teams call" / "**PHOTOGRAPHERS**". Footage: photographers waiting outside a building.
2. "When and where to" / "**SHOW UP**". Footage: a celebrity arriving at an outdoor venue as cameras surround them.
3. "Celebrity looks" / "**PERFECT**". Footage: a celebrity walking, posing slightly for cameras.

## Motion
- 0.0 s: card 1 is already in place, with a slow drift.
- On "they tell them": the card swaps with a quick tilt-spin. It rotates ~-12° and lifts toward camera as the content changes to card 2, then settles straight with a small bounce.
- On "the celebrity then appears": the same swap to card 3, a bit gentler. Hold to the end, with the footage still playing.

## Sound
A soft "card flip" whoosh with a small paper snap on each swap. Faint camera shutter bursts under the footage. A low ambient pad.

## Images — the only thing you may ask about
Before building, send one short message listing the three short footage clips described (paparazzi waiting, a celebrity arriving, a celebrity walking and posing) plus the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source generic paparazzi-style footage.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
