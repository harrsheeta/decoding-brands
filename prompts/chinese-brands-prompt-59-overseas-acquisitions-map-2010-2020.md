# PROMPT 59 — Overseas Acquisitions Map 2010 2020 (map_timeline_animation, 3.8 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (map_timeline_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `map_timeline_animation_4K_sfx.mp4` (sound effects only) and `map_timeline_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~3.8 s).

## Show look — "Decoding Brands" (Zero01 Network), China-brands episode
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

Expected transcript (Whisper hears "acquisitions" as "accolades"):
> …companies spent more than a couple of hundred billion dollars on overseas acquisitions [0.0–3.4].

## Look — cream background with a very faint dot grid
- A world map (Robinson projection, ~1800 px wide, top-aligned) filled with a salmon-orange gradient: darker on the west (#E07B55), lighter on the east (#F6C9A6). Thin cream borders between countries.
- **Timeline across the bottom (y ≈ 1000):** "2010" at the left and "2020" at the right (Bold Italic, ~20 px). A green dashed line (#13875E) runs between two solid green dots, with a green tag/pin marker riding on the line.

## Motion
- The marker slides from 2010 to 2020 across the whole clip (linear with a slight ease at the ends).
- As it passes each year, a small white logo label (white rounded box, thin outline, small logo, ~70 x 24 px) pops onto the map at the target company's location, marking a Chinese overseas acquisition:
  - Volvo (Sweden, 2010)
  - AMC Theatres (US, 2012)
  - Smithfield (US, 2013)
  - Motorola Mobility (US, 2014)
  - Club Med (France, 2015)
  - Pirelli (Italy, 2015)
  - GE Appliances (US, 2016)
  - Legendary (US, 2016)
  - Syngenta (Switzerland, 2017)
  - CPFL Energia (Brazil, 2017)
- Keep the labels from overlapping (offset the US cluster with short leader lines).
- Slow, gentle push-in over the clip.

## Sound
A soft ticking clock for the timeline, a small "pin drop" pop for each logo, and a low ambient pad.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the acquired-company logos listed above (and the Zero01 / Decoding Brands logos), or you should source them. Draw the map and timeline in code. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
