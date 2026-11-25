# PROMPT 87 — Smartwatch VR Headset 3D (3d_objects, 6.5 s, Decoding Brands — Meta glasses)

Copy everything below this line into a new chat and attach the VO clip (3d_objects audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `3d_objects_4K_sfx.mp4` (sound effects only) and `3d_objects_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~6.5 s).

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

Expected transcript (it ends mid-word):
> Some people said it would be smartwatches [0.0–1.9] and some of them said it would be VR headsets [2.2–3.8]. But today, most tech companies and p… [4.7–6.5]

## Look — dark background with a soft diagonal light beam from the top-left and a vignette

## Beats
1. **0.0 → ~1.0 s:** a photoreal 3D Apple Watch (natural titanium, light sport loop, orange action button) slowly rotates at the centre, its display catching light.
2. **"smartwatches" (~1.1 → ~2.2 s):** behind the watch, huge white bold condensed text "SMART WATCH" (~110 px, soft white glow) fades in. The watch overlaps the middle letters.
3. **"VR headsets" (~3.3 → ~4.2 s):** the watch spins away and an Apple Vision Pro headset (dark glass front, light band) rotates in at the centre. The text switches to "VR HEADSETS".
4. **"But today" (~4.3 → ~4.9 s):** the headset and text spin out into darkness, leaving only two thin glowing rim-light arcs that fade.
5. **~4.9 → ~5.3 s:** a quick white flash panel with the "xreal" logo (smart glasses brand) zooms past the camera.
6. **~5.3 s → end:** a full-frame portrait clip of a young man wearing thick-framed smart glasses, lit with a vivid green background and green rim light, with a slow push-in.

## Sound
A deep tech hum, a smooth "turntable" rotation sound for each 3D object, a glowing text swell, a whoosh-out, a bright flash "zip" for xreal, and a confident bass hit on the green portrait.

## Images — the only thing you may ask about
Before building, send one short message listing (1) a 3D model or turntable footage of an Apple Watch, (2) the same for Apple Vision Pro, (3) the xreal logo, (4) a clip of a young man in smart glasses on a green background, (5) the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source or create them. If I don't reply, source or create them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
