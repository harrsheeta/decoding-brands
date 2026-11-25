# PROMPT 78 — YouTube 40B Bloomberg Article (article_animation_1, 4.6 s, Decoding Brands — YouTube Premium)

Copy everything below this line into a new chat and attach the VO clip (article_animation_1 audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `article_animation_1_4K_sfx.mp4` (sound effects only) and `article_animation_1_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~4.6 s).

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
> YouTube makes most of its money through ads [0.0–1.9]. It's around $40 billion every… [2.6–4.6]

## Note
This overrides my saved "article animation" rules. Follow exactly what's below.

## Look — white background with a faint square grid (~#EFEFEF lines, ~60 px), fading out toward the centre

## Beats
1. **0.0 → ~1.0 s:** a Bloomberg article card (~260 x 240 px) sits centred:
   - yellow (#FFF200) masthead strip with "Bloomberg" in black Bold
   - black page body with a white Bold headline: "YouTube Generated $40 Billion in Sales in the Past Year, CEO Says"
   - a photo of a phone showing the YouTube logo with white earphones on a red knit blanket
   - tiny grey byline and date lines
2. **"makes most of its money through ads" (~1.0 → ~2.4 s):** two more article pages fan out behind it, slightly rotated: an Adweek page on the left (tilted −6°, large "Yo…" headline) and a Times of India page on the right (tilted +6°, "OF INDIA" masthead, dark serif text). The stack eases bigger.
3. **"It's around $40 billion" (~2.4 s → end):**
   - The camera zooms in hard (~3x) on the Bloomberg headline, centred on "$40 Billion".
   - On "$40 billion", a yellow highlight (#FFE45C) sweeps behind "$40 billion" in one continuous left → right pass, the text turning black on it. Hold.

## Sound
A paper shuffle for the fan-out, a whoosh on the zoom-in, and a marker swipe for the highlight.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload screenshots of the Bloomberg, Adweek and Times of India articles (and the Zero01 / Decoding Brands logos), or you should rebuild them in HTML with real-looking text and a sourced phone/YouTube photo. If I don't reply, rebuild them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
