# PROMPT 83 — EssilorLuxottica Brands Grid 3pct (logos_and_company_highlight_graph, 3.6 s, Decoding Brands — Meta glasses)

Copy everything below this line into a new chat and attach the VO clip (logos_and_company_highlight_graph audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `logos_and_company_highlight_graph_4K_sfx.mp4` (sound effects only) and `logos_and_company_highlight_graph_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~3.6 s).

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

Expected transcript (Whisper mishears "EssilorLuxottica"):
> …and Meta has now bought a small stake in that very EssilorLuxottica [0.0–3.4].

## Look — cream background with a faint grid and a soft white radial glow at the centre

## Beats
1. **0.0 → ~0.8 s:** a 5 x 5 grid of dark-green tiles (#0E5A3C, ~60 px squares, ~8 px gaps), centred, each holding a white eyewear brand logo from the EssilorLuxottica portfolio:
   - Row 1: Ray-Ban, Oakley, Vogue Eyewear, Prada, Armani
   - Row 2: Versace, Chanel, LensCrafters, Persol, Brooks Brothers
   - Row 3: Sunglass Hut, Arnette, Burberry, Costa, Michael Kors
   - Row 4: Oliver Peoples, Coach, Dolce&Gabbana, Pearle Vision, Ralph Lauren
   - Row 5: Target Optical, Varilux, Swarovski, Tiffany & Co., Transitions
2. **"Meta has now bought" (~0.8 → ~1.9 s):** the logos fade out tile by tile from the bottom-right (tiles dim to plain green), while the camera pushes in and pans so the grid's top-left sits at the centre-right.
3. **"a small stake" (~1.9 s → end):** the top-left tile flips to Meta blue (#3E8EF7) with the white Meta infinity mark. A thin dark curved arrow draws from that tile to the left, ending at a label:
   - "Acquired" (Regular, ~28 px, black) on "bought"
   - "**3%**" (dark-green bold condensed, ~80 px) and "***Stake***" (green Bold Italic, ~44 px) on "stake"
   Hold.

## Sound
A quick tile-ripple tick as the logos clear, a whoosh on the push, a satisfying flip "clack" on the Meta tile, a pen-draw for the arrow, and a soft hit on "3%".

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the 25 brand logos listed (white versions), the Meta logo and the Zero01 / Decoding Brands logos, or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
