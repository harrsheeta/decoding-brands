# PROMPT 45 — USA Attention Celebrity Mosaic (map_scale_animation_with_tiles, 8.3 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (map_scale_animation_with_tiles audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `map_scale_animation_with_tiles_4K_sfx.mp4` (sound effects only) and `map_scale_animation_with_tiles_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~8.3 s).

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
> In the US [0.0–0.3], people's attention is distributed across hundreds of A-listers [0.8–4.0]. Actors [4.7], musicians [5.2], athletes [5.9], comedians [6.5], etc. [7.0] All of them… [7.7–8.1]

## Scene 1 — USA attention map (0.0 → ~2.5 s)
- Light grey background with a soft diagonal light falloff (white top-left, grey corners).
- A centred tile board (~11 x 6 square tiles, ~60 px) in salmon #F0A58A with thin golden-yellow borders. Over it, a solid black silhouette of the contiguous USA.
- On "US": black letter tiles flip in at the centre, spelling "U S A" (white bold letters on black tiles).
- On "attention": a row of green tiles (#3E9A7A) flips in one by one, spelling "A T T E N T I O N" across the map's middle. A thin green line runs under it.

## Scene 2 — the A-lister mosaic (~2.5 → ~4.4 s)
- Hard cut with a light RGB-split glitch to a full-frame mosaic of ~40 Hollywood and US celebrity headshots (8 x 5 grid, thin dark gaps), with a slight blue chromatic fringe on the edges.
- Tiles flip in quickly, starting as white flashes. The camera drifts slowly.

## Scene 3 — categories (~4.0 → ~7.6 s)
On each word, cut to a 2 x 2 grid of four photos with a huge bold condensed title across the middle (white-grey 3D extruded letters, ~140 px, with a blue/cyan offset shadow):
- "A - LISTERS" on "A-listers"
- "ACTORS" on "actors"
- "MUSICIANS" on "musicians"
- "ATHLETES" on "athletes"
- "COMEDIANS" on "comedians"

## Scene 4 — "All of them" (~7.7 → end)
Back to the full mosaic, slightly zoomed out, with tiles shimmering. Hold.

## Sound
A soft tile-flip clack for each letter, a glitch burst on the cut, rapid camera-shutter flicks for the mosaic, a punchy bass hit on each category title, and a low pad.

## Images — the only thing you may ask about
Before building, send one short message listing (1) ~40 US celebrity headshots, (2) 4 photos each for actors, musicians, athletes and comedians, (3) the Zero01 Network and Decoding Brands logos, and ask whether I'll upload them or you should source them. Draw the USA map and tiles in code. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
