# PROMPT 75 — What vs Where Light Beam (light_beam_motion_graphics, 4.3 s, Decoding Brands — YouTube Premium)

Copy everything below this line into a new chat and attach the VO clip (light_beam_motion_graphics audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `light_beam_motion_graphics_4K_sfx.mp4` (sound effects only) and `light_beam_motion_graphics_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~4.3 s).

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

Expected transcript (it starts mid-sentence):
> …is not just focusing on what people are watching [0.0–1.7], but also where people are watching it [1.8–4.3].

## Look — cream background
- Large soft beige light-beam wedges (#F3E3C0, ~50% opacity) cut diagonally across the frame, as if light is shining from the YouTube logo.
- The YouTube logo (red rounded rectangle with a white play triangle, ~100 x 70 px, soft shadow) sits just left of centre.
- **Content cards:** white rectangles (~200 x 110 px) with a 4 px green (#13875E) border on two sides, fanned out to the LEFT inside the beam, receding in perspective (bigger at the back-left, overlapping).
- **Device icons:** clean black line icons (~3 px strokes, white fills): a TV/monitor on a stand, a smartphone, a tablet.

## Beats
1. **"not just focusing on what people are watching" (0.0 → ~1.7 s):**
   - The cards slide out from behind the logo one by one along the beam (~0.2 s apart).
   - Right of the logo, a stacked text block reveals word by word: "*Not just*" (black Italic) / "**FOCUSING ON**" (green condensed caps) / "*what*" (Italic) / "***people*** *are*" / "**WATCHING**" (green condensed caps, right-shifted).
2. **"but also where people are watching it" (~1.8 s → end):**
   - The beam swings to point RIGHT. The cards slide back into the logo and the text clears.
   - The device icons pop in to the right of the logo inside the new beam: monitor, then phone, then tablet.
   - Left of the logo, a new text block: "*Also*" / "**WHERE**" (green caps) / "***people*** *are*" (and "watching" if the VO reaches it). Hold.

## Sound
A soft "projector light" swell when the beam appears, card slide flicks, a whoosh as the beam swings, a soft tech blip for each device, and ticks per word.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the YouTube logo and the Zero01 / Decoding Brands logos, or you should source them. Draw the cards, beams and device icons in code. If I don't reply, source the logos yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
