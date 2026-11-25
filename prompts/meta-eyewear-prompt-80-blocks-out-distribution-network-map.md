# PROMPT 80 — Blocks Out Distribution Network Map (metamotiongraphics, 8.8 s, Decoding Brands — Meta glasses)

Copy everything below this line into a new chat and attach the VO clip (metamotiongraphics audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `metamotiongraphics_4K_sfx.mp4` (sound effects only) and `metamotiongraphics_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~8.8 s).

## Show look — "Decoding Brands" (Zero01 Network), Meta smart-glasses / EssilorLuxottica episode
Ignore my saved Jet Airways / Meta / idk / dairy themes and any saved article rules; follow ONLY this look.
- **Watermarks on every frame:**
  - top-left: the "ZERO01⚡NETWORK" logo (small, ~22 px tall, 30 px from the edges; white on dark scenes, dark on light scenes)
  - top-right: the "DECODING BRANDS" yellow-green badge (~60 px)
- **Backgrounds** (each clip says which):
  - **Dark:** near-black #0B0B0B → #1A1A1A with a soft vignette.
  - **Cream:** #FBF4E6 with a very faint vertical line texture (thin lines ~4% darker, ~6 px apart, fading out toward the centre).
  - **White:** #FFFFFF.
  - **Desktop:** a macOS El Capitan / Yosemite sunset-mountain wallpaper.
- **Type:**
  - Neue Haas Grotesk / Helvetica Neue (fallback Inter) for body, labels and UI.
  - For big labels: a bold condensed sans (Bebas Neue / Barlow Condensed Bold) in caps, often with a small black italic "kicker" word above (e.g. *World's* / FACTORY).
- **Accent colours:** green #13875E (card borders, big labels), China red #D7262B, gold #F2B866.
- **Video cards:** rounded corners (~12 px) with a ~4 px green #13875E border on cream scenes; plain square tiles on dark scenes.
- **B-roll:** "b-roll" means short real video clips. Play them inside their cards/tiles; never use still frames when a clip is available.
- **Motion:** smooth, eased (ease-out quint, small overshoot on pops), with gentle constant camera drift. Text reveals follow the VO word by word.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on its word.

Expected transcript (it ends mid-sentence):
> Meta essentially gets to block out every other tech company [0.0–3.1] from accessing that very distribution network [3.5–5.8] that the world's single biggest eyewear manufacturer… [6.1–8.8]

## Scene 1 — the rolling circles (0.0 → ~2.0 s), dark charcoal background (#1F1F1F) with a vignette
- Big green circles (~560 px diameter, radial gradient #3AA57E → #1F7A57) roll horizontally across the frame from right to left, like a conveyor, with white Bold text centred in each:
  - "Meta blocks out" (on "Meta … block out")
  - "every tech companies" (on "every other tech company")
- At ~1.5 s a small light-blue bubble with the blue Meta infinity mark rises from the bottom-centre, with a peach circle rising behind it.

## Scene 2 — distribution network (~2.0 s → end)
- Cut to a dotted world map: continents made of small grey square dots (#3D3D3D) on charcoal.
- About 10 green node dots (#3FBF8F) sit across the continents (N. America, S. America, Europe, Africa, Middle East, India, China, SE Asia, Australia), joined by thin white curved arcs (~40% opacity) that draw on like a network.
- On "accessing" the Meta bubble (light-blue disc #BFE3FF with the blue infinity mark, soft glow) pops in at the map's centre.
- Text under the map, centred, revealed word by word (grey → white): "Distribution network by **world's biggest**" then, on a second line, "***eyewear manufacturer***".
- Very slow drift. Hold.

## Sound
A rolling "whoosh-thud" for each circle, a bubble pop for the Meta logo, a soft network "connect" shimmer as the arcs draw, and ticks for the words.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the Meta logo and the Zero01 / Decoding Brands logos, or you should source them. Draw the map, nodes and circles in code. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
