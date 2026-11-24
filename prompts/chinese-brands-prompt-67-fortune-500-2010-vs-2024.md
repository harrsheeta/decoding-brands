# PROMPT 67 — Fortune 500 2010 vs 2024 (website_scroll_ui_animation, 11.8 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (website_scroll_ui_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `website_scroll_ui_animation_4K_sfx.mp4` (sound effects only) and `website_scroll_ui_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~11.8 s).

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
> Look at this chart. In 2010 [0.0–1.0], less than 50 Chinese companies were in the list of Fortune 500 companies in the world [1.7–6.0]. But fast forward to today [6.6–7.3], there are around 130 Chinese companies in that same list [7.9–11.3].

## Look — white background
Fortune Global 500 list pages in strong 3D perspective (tilted ~25° on X and ~-15° on Z, like paper lying on a desk at an angle), with a slight depth-of-field blur at the far edge.
- Page style: "FORTUNE" masthead in bold condensed black, the year in grey under it, a red "Company" column header and a red "Revenue ($M)" header.
- Rows on alternating light-grey bands: rank, company name and revenue, in a condensed font.

## Beats
1. **"In 2010" (0.0 → ~1.6 s):** the camera starts close on the "FORTUNE 2010" masthead, angled.
2. **"less than 50 Chinese companies…" (~1.7 → ~6.4 s):** the camera scrolls smoothly down the 2010 list, showing only the Chinese companies with their real 2010 ranks and revenues: China Petrochemical, State Grid, China National Petroleum, China Mobile, ICBC, China Construction Bank, China Life, China Railway Construction, China Railway Group, Agricultural Bank of China, Bank of China, China Southern Power Grid, Dongfeng Motor, and so on.
3. **"fast forward to today" (~6.6 → ~7.6 s):** the 2010 page flies off. A "FORTUNE 2024" page swings in from the top-right in 3D (rotating into place).
4. **"around 130 Chinese companies" (~7.9 s → end):** a fast, accelerating scroll down a much longer 2024 list of Chinese companies. Some rows have a pale-blue highlight band. Motion blur at speed. It ends still scrolling.

## Sound
A page-swing "whoosh" for each list, soft paper scroll friction, and a fast tick-tick-tick that accelerates on the 2024 scroll.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the Fortune logo / reference screenshots of the 2010 and 2024 Global 500 lists and the Zero01 / Decoding Brands logos, or you should build the lists from the real data yourself. If I don't reply, build them yourself from the real Fortune Global 500 data.

## Numbers
Keep the VO's figures: fewer than 50 in 2010, around 130 today.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
