# PROMPT 76 — Premium Subscribers Graph to 2Cr Card (graph_to_infographic, 8.8 s, Decoding Brands — YouTube Premium)

Copy everything below this line into a new chat and attach the VO clip (graph_to_infographic audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `graph_to_infographic_4K_sfx.mp4` (sound effects only) and `graph_to_infographic_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~8.8 s).

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

Expected transcript (it ends mid-sentence):
> And yet, in just 2023 [0.0–1.2], YouTube added 2 crore new premium subscribers globally [2.2–4.5]. That is 2 crore of its best users [5.3–7.0] completely removed from… [7.4–8.8]

## Look — cream background with a faint dashed grid (~#E8DCC4)

## Beats
1. **The chart (0.0 → ~2.8 s):**
   - The title fades in at the top-left: "*YouTube*" (black Italic, small) over "**PREMIUM SUBSCRIBERS**" (green condensed caps, ~34 px).
   - Thin grey axes draw, with a small rotated y-axis label "Number of subscribers in millions" and years 2020–2024 on the x-axis.
   - Pale-yellow bars (#F9D58A) grow up one after another with real YouTube Music + Premium subscriber counts: 2020 ≈ 30M, 2021 ≈ 50M, 2022 ≈ 80M, 2023 ≈ 100M, 2024 ≈ 125M.
2. **"added 2 crore new premium subscribers globally" (~2.8 → ~5.2 s):**
   - The camera pushes into the 2023 bar. Its top section (the 2023 increase) is labelled "**2 CR**" in white Bold.
   - A thin black dashed arrow loops out from the bar's top with a curl and points to a label to its right: "*New*" / "*Premium*" / "*Subscribers*" (Italic, stacked), then "**GLOBALLY**" (big green condensed caps) on "globally".
3. **"That is 2 crore of its best users" (~5.3 → ~7.2 s):**
   - The chart slides away left. The bar becomes a square pale-yellow card (~280 x 230 px), centre-right, with "**2 Cr.**" (white Bold, ~52 px) and "**Best Users**" (white Bold, ~28 px).
   - On the left, a curved "cylinder" wall of b-roll tiles (people watching phones and laptops, ~10 tiles in perspective, bending away) slides in.
   - Inside the lower part of the card, a b-roll plays: two men working on laptops at a café.
4. **"completely removed from…" (~7.4 s → end):**
   - Under the card, at the right, "*Removed from*" (black Italic, small) over "**Ad Economy**" (green Bold, ~32 px) types in.
   - Then the card's footage flattens into a solid YouTube-red (#E31B23) silhouette of the same two people at laptops, as if they've been cut out of the ad world. Hold.

## Sound
A rising tone for each bar, a whoosh on the push-in, a pen "squiggle" for the dashed arrow, a soft "whomp" as the bar becomes the card, café ambience under the b-roll, and a muted, hollow thud when the footage turns into the red silhouette.

## Images — the only thing you may ask about
Before building, send one short message listing (1) ~10 b-roll clips of people watching phones and laptops, (2) a café clip of two men on laptops, (3) the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Numbers
The VO's 2 crore = 20 million new subscribers in 2023 (≈80M → ≈100M). Keep the bars consistent with that.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
