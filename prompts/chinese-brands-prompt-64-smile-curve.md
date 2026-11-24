# PROMPT 64 — Smile Curve (graph_curve_broll_ideas, 14.5 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (graph_curve_broll_ideas audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `graph_curve_broll_ideas_4K_sfx.mp4` (sound effects only) and `graph_curve_broll_ideas_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~14.5 s).

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

Expected transcript:
> See, in the field of economics, there is an interesting concept called the smile curve [0.0–3.2]. At the higher ends of the smile, you have things like design, R&D and also marketing and branding [3.8–8.0], which basically capture most amount of value [8.3–10.1], and at the bottom of the smile is manufacturing [10.6–12.1]. The problem with China was that… [13.2–14.5]

## Beats — black background
1. **0.0 → ~1.2 s:** thin white L-shaped axes draw (the vertical first, then the horizontal), with the origin at the bottom-left.
2. **"concept called the smile curve" (~1.3 → ~2.6 s):** "The Smile Curve" (white Medium, ~40 px) types in at the centre. A gold U-curve (#F2B866, ~3 px, arrowheads at both ends pointing up and out) draws outward from its bottom centre to both ends.
3. **~2.7 → ~3.7 s:** the axes fade. The camera pushes in on the curve.
4. **"design, R&D" (~3.8 → ~6.8 s):** the camera pans to the upper-left end of the curve. A vertical b-roll strip (~160 x 360 px) of engineers in a lab slides up at the left edge. Next to the arrow tip, "**Design**" appears, then "&" (small), then "**R&D**" (white Bold, ~44 px) on their words.
5. **"marketing and branding" (~7.0 → ~8.2 s):** the camera pans right to the upper-right end. A vertical b-roll strip of a giant LED billboard in a Chinese city appears at the right edge, with "**Marketing**" and "& **Branding**" beside the arrow tip.
6. **"capture most amount of value" (~8.3 → ~10.4 s):** the camera pulls back to show the whole smile, with both labels smaller at its two ends. The strips fade.
7. **"bottom of the smile is manufacturing" (~10.6 → ~13.1 s):** the camera tilts down so the curve's bottom fills the top of the frame. "**Manufacturing**" sits centred just under it, with a wide b-roll strip (~540 x 130 px) of factory robots below.
8. **~13.2 s → end:** cut to my talking-head footage for "The problem with China was that…". If I don't provide it, end on a fade to black.

## Sound
A pen-draw "zip" for the axes and curve, soft typing for the title, a whoosh on each pan, a subtle positive chime on "value", industrial clank ambience under "Manufacturing", and a low pad throughout.

## Images — the only thing you may ask about
Before building, send one short message listing (1) a b-roll clip of engineers in a lab, (2) a Chinese city LED billboard clip, (3) a factory robots clip, (4) my talking-head clip for the last ~1.3 s (optional), (5) the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source the b-roll and skip the talking head.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
