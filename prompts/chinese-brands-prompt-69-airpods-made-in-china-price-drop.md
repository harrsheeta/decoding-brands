# PROMPT 69 — AirPods Made In China Price Drop (UI_animations, 8.2 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (UI_animations audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `UI_animations_4K_sfx.mp4` (sound effects only) and `UI_animations_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~8.2 s).

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

Expected transcript (the VO starts at ~3.1 s; the first 3 s have no VO):
> Now, what if I told you that this was made in China [3.1–5.0], would the price that you had in mind suddenly drop? [5.9–7.5]

## Look — macOS desktop
El Capitan sunset-mountain wallpaper. Safari-style windows with traffic-light dots and URL bars, plus soft shadows.

## Beats
1. **0.0 → ~1.8 s (no VO):** an "Apple AirPods Pro 2" buy page window ("Free Engraving / Buy AirPods Pro 2 / Personalise them for free", with the white AirPods case) sits at the top-left. More retailer windows (Croma, Amazon, Flipkart AirPods Pro 2 pages) fly in and pile up around it at slight angles.
2. **~1.8 → ~2.7 s:** the camera zooms into the main window's price card: "MRP ₹XXXXX (Incl. of all taxes)", a grey "Add to Cart" button, and a lilac "Buy Now" button (#B7A6F2). A mouse cursor glides to "Buy Now" and hovers.
3. **~2.7 → ~3.1 s:** all the windows get sucked away in a fast swirl with motion blur (a tornado / genie effect), leaving the empty desktop.
4. **"what if I told you that this was made in China" (~3.1 → ~5.5 s):** a macOS blue folder icon labelled "Made in China" pops in at the centre (bounce), then slides to the bottom-right and shrinks.
5. **"would the price that you had in mind" (~5.9 → ~7.0 s):** the AirPods window slides back in at the centre, faint at first, then solid, now showing "MRP ₹ 17999".
6. **"suddenly drop?" (~7.0 s → end):** the camera punches in on the price, and the number rolls down (odometer flip) to "**MRP ₹ 2239**". Hold.

## Sound
A soft click for each window landing, a cursor hover tick, a big swirl "whoosh-suck", a Finder "pop" for the folder, a window whoosh, and a descending "slot roll" ending in a small thud on ₹2239.

## Images — the only thing you may ask about
Before building, send one short message listing (1) an El Capitan wallpaper, (2) AirPods Pro 2 retailer page screenshots (Apple, Croma, Amazon, Flipkart) or permission to rebuild them in HTML, (3) the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source or create them. If I don't reply, rebuild the pages in HTML yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
