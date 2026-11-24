# PROMPT 35 — Parasocial Relationship Definition (text_based_animation, 13.4 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (text_based_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `text_based_animation_4K_sfx.mp4` (sound effects only) and `text_based_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~13.4 s).

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
> See, that is where something called parasocial relationships come into the picture [0.0–3.3]. For those of you who do not know [3.8–4.6], parasocial relationships are simply one-sided emotional connections [5.1–8.0] where you feel very close to somebody [8.7–10.4], while that somebody does not even know that you exist [11.2–13.2].

## Scene 1 — title (0.0 → ~3.4 s)
- Dark background. Two warm cinematic photos sit as a wide band across the middle: left, a smaller one of a young man in a hoodie at night, hands clasped at his mouth, thinking (warm lamp light); right, a larger one of a curly-haired young man in an orange hoodie looking down, with a hard window light.
- The band drifts slowly left.
- On "parasocial relationships": a big title in cream #F1EFC6 (Neue Haas Medium, ~120 px, very tight leading), "Para-Social" over "Relationship", reveals letter by letter over the gap between the photos and overlapping them.
- Every "o" in the title is replaced by a speech-bubble shape (a cream filled circle with a small tail).

## Scene 2 — A-roll (~3.4 → ~4.6 s)
Cut to my talking-head clip for "For those of you who do not know". Use the footage I give you; if I don't give any, leave this section as a plain dark-background pause with the title faded out.

## Scene 3 — dictionary definition (~4.6 → end)
- A dictionary entry in cream, set very large, so the camera has to travel along it:
  - the headline "Para-Social Relationship" (~120 px), partly off the top-left
  - the phonetic line "/ˌpærəˈsəʊʃəl rɪˈleɪʃnʃɪp/" (~56 px)
  - "*noun*" (italic, ~70 px)
  - the definition (~64 px, two long lines): "one sided emotional connection, where you feel very close to somebody, while that somebody does not even know that you exist."
- The definition words fill from grey to cream with the VO.
- The camera tracks horizontally along the line, keeping the currently spoken word near the centre, with soft depth blur at the frame edges.
- On "does not even know that you exist", the camera eases back to frame the whole entry (left-aligned, slightly cropped on the right). The final words fill in. Hold.

## Sound
A soft low pad. A subtle "type" tick per title letter. A gentle whoosh into the definition, and a smooth sliding air sound under the camera track.

## Images — the only thing you may ask about
Before building, send one short message listing (1) the two moody young-man photos described, (2) my talking-head clip for 3.4–4.6 s (optional), (3) the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source the photos (generic people, not real identifiable ones) and leave the A-roll gap.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
