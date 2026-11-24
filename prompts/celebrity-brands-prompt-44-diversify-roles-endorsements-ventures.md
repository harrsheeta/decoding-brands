# PROMPT 44 — Diversify Roles Endorsements Ventures (broll_animation, 5.7 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (broll_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `broll_animation_4K_sfx.mp4` (sound effects only) and `broll_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~5.7 s).

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

Expected transcript (it starts and ends mid-sentence):
> …to diversify across roles [0.0–1.1], endorsements [1.8] and even ventures [2.4–3.0], just so that they stay relevant [3.6–4.9].

## Look and beats
- Black background with a soft vignette.
- **0.0 s:** "Diversify across" (white Regular, ~30 px) sits centred.
- **On "roles":** the text slides left as a white-outlined box appears to its right and the word "**Roles**" (Bold) decodes into it (random-character scramble, ~0.3 s). At the same moment a row of 3 equal photo tiles (~150 x 190 px, square corners) pops in under the text, centred: three photos of one actress in very different film roles.
- **On "endorsements":** the box widens and the word scrambles to "**Endorsements**". The photos swap one at a time with a quick white flash per tile: an actor in three different brand ads.
- **On "ventures":** the box scrambles to "**Ventures**". The photos swap to one actor at events for his own brand and ventures.
- **"just so that they stay relevant":** hold, with a slow camera push (1.0 → 1.05).

## Sound
A digital decode chatter for each word swap, a camera-flash "pop" for each photo flash, and a low pad.

## Images — the only thing you may ask about
Before building, send one short message listing (1) 3 photos of one actress in different film roles, (2) 3 photos of an actor in brand endorsements, (3) 3 photos of an actor at his own brand/venture events, (4) the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. (Reference: Alia Bhatt for roles, Ranveer Singh for endorsements, Hrithik Roshan / HRX for ventures.) If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
