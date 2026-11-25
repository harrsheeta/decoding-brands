# PROMPT 84 — Sunglass Hut 17000 Stores (match_cut_and_text, 4.9 s, Decoding Brands — Meta glasses)

Copy everything below this line into a new chat and attach the VO clip (match_cut_and_text audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `match_cut_and_text_4K_sfx.mp4` (sound effects only) and `match_cut_and_text_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~4.9 s).

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

Expected transcript (it starts mid-list):
> …Sunglass Hut, etc. [0.0–0.5], and all in all, they have more than 17,000 physical stores [0.7–4.3].

## Look — cream background with a faint embossed pattern of sunglasses outlines (~6% darker), drifting slowly

## Beats
1. **Match cut (0.0 → ~1.5 s):** a b-roll card (~430 x 230 px, rounded, 4 px green #13875E border, soft shadow) cuts quickly between 3–4 different Sunglass Hut storefronts (mall stores with lit signs), ~0.35 s each. The "sunglass hut" sign stays in the same spot at the top-centre of every shot.
2. **~1.5 → ~2.3 s:** the card crops down (top and bottom close in) until only the store's sign band remains. It then becomes a clean black rounded box with the white Sunglass Hut logo (sun circle + "sunglass hut").
3. **"more than 17,000" (~2.5 → ~3.5 s):** the logo box turns into five dark-green tiles (#0E4F3A, white digits, ~60 px each) that roll like an odometer/split-flap and lock as "1 7 0 0 0" left → right.
4. **"physical stores" (~3.9 s → end):** "*Physical*" (black Italic, ~26 px) fades in above the tiles' left edge. Hold.

## Sound
A quick camera-shutter cut on each store, a soft "snap" as the card crops, an odometer clatter with locking clicks, and a soft chime on "Physical".

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload 3–4 Sunglass Hut storefront clips or photos and the Sunglass Hut and Zero01 / Decoding Brands logos, or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
