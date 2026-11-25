# PROMPT 86 — Glasses Directions Translate Photos Queries (cool_brolls, 13.4 s, Decoding Brands — Meta glasses)

Copy everything below this line into a new chat and attach the VO clip (cool_brolls audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `cool_brolls_4K_sfx.mp4` (sound effects only) and `cool_brolls_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~13.4 s).

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

Expected transcript:
> And these glasses could show you directions while you're driving or walking [0.0–3.3], could translate languages or signs [3.9–5.2], could let you take photos without really taking out your phone [5.9–8.1], and even answer general queries without really requiring you to take out your device [9.0–13.1]…

## Look — dark background (#0E0E0E) with a faint square grid (#1C1C1C, ~150 px)

## Beats
1. **0.0 → ~1.3 s:** 5–6 small b-roll tiles float scattered across the grid (a person driving with glasses, a woman walking, two people talking, a man at a desk), drifting slightly.
2. **"show you directions" (~1.3 → ~3.7 s):** the tiles fly away and one centred card (~470 x 300 px) zooms forward: a man wearing Ray-Ban Meta glasses while driving. Above its top-left: "Could Show You" (white Regular, ~26 px). Below its bottom-right: "***Directions***" (gold #F2C66B, Bold Italic, ~34 px).
3. **"translate languages" (~3.9 → ~5.7 s):** the card swaps (quick scale-blur): two people talking on a pink background with a phone showing a translation UI. Labels "Translate" / "***Languages***".
4. **"take photos" (~5.9 → ~8.8 s):** a woman in a purple jacket posing between modern buildings, a photo-capture UI flash. Labels "Could Let You Take" / "***Photos***".
5. **"answer general queries" (~9.0 s → end):** a man in sunglasses talking on a city terrace, then a man in a grocery aisle holding an orange and asking his glasses. Labels "***Answer*** Your" / "***Queries***".
- Each label swap reveals word by word with the VO. Gentle drift throughout.

## Sound
A UI whoosh for each card swap, a soft "chime" as each gold word lands, and subtle city/ambient sounds under each b-roll.

## Images — the only thing you may ask about
Before building, send one short message listing Ray-Ban Meta ad-style clips for: driving with directions, live translation between two people, taking photos hands-free, asking the glasses a question (on a terrace and in a grocery store), plus 5–6 extra floating clips and the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
