# PROMPT 77 — Premium Door Ad Searchlight (creative_visuals_youtube_door, 9.5 s, Decoding Brands — YouTube Premium)

Copy everything below this line into a new chat and attach the VO clip (creative_visuals_youtube_door audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `creative_visuals_youtube_door_4K_sfx.mp4` (sound effects only) and `creative_visuals_youtube_door_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~9.5 s).

## Show look — "Decoding Brands" (Zero01 Network), YouTube Premium episode
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

Expected transcript:
> The thing is, the moment somebody pays for YouTube Premium [0.0–2.1], they completely vanish from YouTube's ad ecosystem [2.8–5.4]. YouTube advertisers cannot target them, no matter how hard they try [5.7–9.2].

## Look
- Background: a dark warm charcoal-brown (#1E1B16 at the centre → near-black edges), with a heavy vignette and faint floating dust specks drifting slowly.
- Everything is in a flat paper-cutout style (layered card shapes with subtle shading and soft drop shadows).

## Beats
1. **"the moment somebody pays for YouTube Premium" (0.0 → ~2.3 s):**
   - Centre: a red door (#B3121B, with panel details and a gold frame) standing open toward the right. Bright warm white light pours out of the doorway and casts a glow on the floor.
   - A red/orange paper-cutout person (geometric limbs, flat shaded) walks into the doorway with a simple 2–3 pose walk, getting smaller as they step into the light.
2. **"they completely vanish from YouTube's ad ecosystem" (~2.4 → ~5.6 s):**
   - The person disappears into the light. The door swings shut (~2.8 s), showing a small "YouTube Premium" logo plate on it.
   - On "vanish", the light around the door fades and the door itself dissolves into the darkness. By ~4.0 s the frame is empty, just dust and darkness.
3. **"YouTube advertisers cannot target them" (~5.7 → end):**
   - A "searchlight" flies up from the bottom and settles just right of centre. It's made of stacked brand logo tiles: the YouTube logo as the lamp head, with Netflix, Amazon and Coca-Cola logo tiles stacked behind it as the body.
   - It emits a red light cone (#E31B23, soft-edged, fading to transparent) that sweeps around searching: first left, then down, then right (~1 s per sweep). It lights up only empty darkness and dust. Hold on the last sweep.

## Sound
A warm "heavenly" swell from the open door, soft footsteps, a heavy door close "thunk", a fading airy "poof" as it dissolves into darkness, silence, then a searchlight "clunk-on" hum and slow mechanical sweeps (servo whirr), all eerie and empty.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the YouTube, YouTube Premium, Netflix, Amazon and Coca-Cola logos and the Zero01 / Decoding Brands logos, or you should source them. Draw the door, figure and light in code (paper-cutout style). If I don't reply, source the logos yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
