# PROMPT 88 — What Will Replace Smartphone Articles (intro_potential_article, 3.0 s, Decoding Brands — Meta glasses)

Copy everything below this line into a new chat and attach the VO clip (intro_potential_article audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `intro_potential_article_4K_sfx.mp4` (sound effects only) and `intro_potential_article_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~3.0 s).

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

Expected transcript (it starts mid-sentence):
> …new prediction about what will replace smartphones and laptops [0.0–3.0].

## Note
This overrides my saved "article animation" rules. Follow exactly what's below.

## Beats — fast whip montage of real articles, each with a strong white vignette at the edges
1. **0.0 → ~0.6 s:** a grey article page (headline about future products, a photo of a speaker on stage) zooms past with heavy motion blur.
2. **~0.6 → ~1.2 s:** a whip-pan to a deep-blue (#1C1A6B) article page: "AI First Devices Are Coming. Could Any of Them Replace the iPhone?" (white serif headline), streaked with vertical motion blur.
3. **~1.2 s → end:** a whip-pan to a white HowStuffWorks-style article: headline "What Will Replace the Smartphone?" (dark navy, Lato Bold, ~60 px), "By: Patrick J. Kiger" in small blue, a thin teal rule, and a photo of planets/marbles below.
   - The camera pushes in hard on the headline.
   - On "replace smartphones" a bright yellow highlight (#F1EE2B) sweeps left → right behind "Replace the Smartphone?" in one continuous pass.
   - Hold with a slow drift.

## Sound
Two fast whip whooshes, a page "snap" landing on the last article, and a marker swipe for the highlight.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload screenshots of the three articles (or permission to rebuild them in HTML) and the Zero01 / Decoding Brands logos, or you should rebuild them yourself. If I don't reply, rebuild them in HTML.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
