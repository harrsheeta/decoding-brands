# PROMPT 82 — Spectacles Without Physical Distribution (cool_brolls_ideas, 6.7 s, Decoding Brands — Meta glasses)

Copy everything below this line into a new chat and attach the VO clip (cool_brolls_ideas audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `cool_brolls_ideas_4K_sfx.mp4` (sound effects only) and `cool_brolls_ideas_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~6.7 s).

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
> If Meta were to suddenly enter a market with a mass consumer product like Spectacles [0.0–4.0], without any meaningful physical distribution [4.3–6.7]…

## Scene 1 — Meta enters (0.0 → ~1.3 s)
- A light grey abstract space: tall white vertical panels (lanes) with thin grey edges, in perspective. The Meta logo (blue disc, white infinity mark, ~110 px) sits in the brightest central lane.
- On "suddenly enter a market" (~0.7 s) the whole scene rotates 90° (the camera rolls), turning the lanes horizontal. The logo slides along its lane to the right.

## Scene 2 — Spectacles (~1.3 s → end), cream background
- Cut to a b-roll card (~470 x 270 px), tilted ~-8° at first, straightening as it settles: a woman putting on Ray-Ban Meta smart glasses.
- The card cuts between shots every ~0.8 s: the same woman walking on a city street, a man in glasses looking up, a close-up of the glasses.
- On "without any meaningful": above the card, "Without any **meaningful**" (Regular + Bold, ~26 px) reveals word by word.
- On "physical distribution": under the card at the right, "***physical distribution***" (Bold Italic, ~30 px) reveals.

Hold.

## Sound
A low whoosh for the camera roll, a soft card slide, quiet street ambience under the b-roll, and ticks for the words.

## Images — the only thing you may ask about
Before building, send one short message listing ~4 short Ray-Ban Meta glasses lifestyle clips (a woman putting them on, walking, a man looking up, close-ups) and the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
