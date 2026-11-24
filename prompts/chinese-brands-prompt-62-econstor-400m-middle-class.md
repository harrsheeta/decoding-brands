# PROMPT 62 — EconStor 400M Middle Class (article_animation_with_broll_in_bg, 4.3 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (article_animation_with_broll_in_bg audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `article_animation_with_broll_in_bg_4K_sfx.mp4` (sound effects only) and `article_animation_with_broll_in_bg_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~4.3 s).

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

Expected transcript (it ends mid-sentence):
> Another thing was that by 2010 [0.0–1.0], more than 400 million middle-class Chinese had… [1.7–3.8]

## Look
- **Background:** full-frame b-roll of Chinese consumer life, darkened to ~35% with a cool grey overlay. A quick cut every ~0.7 s: a Chinese flag waving, a luxury jewellery counter, an eyewear store, a shopper in a boutique, a crowd outside a Rolex store.
- **Article over it:** left-aligned at x ≈ 95, y ≈ 80, with no card. A thick orange vertical bar (#E8743B, ~6 px) runs down its left edge.
  - the EconStor logo ("ECON" white on a black box, "STOR" in green)
  - headline in Bold condensed caps, white (~34 px): "**400 MILLION CHINESE RESIDENTS WITH DISPOSABLE INCOME**"
  - body in Regular, ~17 px, white: "By some estimates, close to 400 million people could be considered middle class or moving out of poverty around 2010, as the income distribution shifted from a pyramid shape (majority poor) to a more olive shape with a growing middle class."
  - date in small italic: "Dec 24, 2017"

## Motion
- 0.0 s: the logo and headline are there in grey.
- The headline fills from grey to white word by word toward "400 million" (on "400 million", "400 MILLION" flashes brighter).
- The body fades in by ~1.0 s.
- Slow push-in throughout.

## Sound
A soft city/mall ambience, a subtle "cut" click on each b-roll change, a soft highlight swell on "400 million", and a low pad.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the background b-roll clips listed above, the EconStor logo, and the Zero01 / Decoding Brands logos, or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
