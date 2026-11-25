# PROMPT 79 — Meta 3pct Article Distribution Tunnel (cool_article_animation, 9.0 s, Decoding Brands — Meta glasses)

Copy everything below this line into a new chat and attach the VO clip (cool_article_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `cool_article_animation_4K_sfx.mp4` (sound effects only) and `cool_article_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~9.0 s).

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
> This move by Meta to invest in the world's largest eyewear company [0.0–2.6] shows how in mature markets [3.0–4.6], distribution could be as important as innovation [5.0–7.3], if not more [8.2–8.6].

## Scene 1 — the article (0.0 → ~3.0 s), white background with a faint large grid (~#EFEFEF, ~120 px)
- A high-contrast black & white photo of Mark Zuckerberg's face (head and shoulders, centred, ~380 px wide) is cut into horizontal strips.
- On "Meta" (~0.4 s) the strips pull apart vertically: the hair/forehead strip slides up, the eyes strip slides down. This opens a white gap in the middle.
- In the gap, the article reveals (centred):
  - headline in Bold Italic, ~30 px, two lines: "Meta takes around 3% stake in Ray-Ban-parent EssilorLuxottica, source says"
  - "The Hindu | 09 July 2025" in small grey italic
  - body in Regular, ~16 px, three lines: "Meta Platforms has acquired a nearly 3% stake in eyewear maker EssilorLuxottica, a source told Reuters on Tuesday, amid growing consumer interest in AI-powered wearable devices."
- A soft warm-yellow circular glow (~50 px, #F9D27A, ~70% opacity, blurred edges) glides along the headline like a reading spotlight, landing on "takes", then "stake", then "parent" with the VO.

## Scene 2 — the tunnel (~3.0 s → end), dark background
- Hard cut to black with a 3D perspective tunnel: thin grey lines (#3A3A3A) run from the frame's corners to an inner rectangle (~460 x 230 px, centred), with a second, larger outline frame.
- Inside the inner rectangle plays b-roll of a white delivery truck driving on a highway at night (light streaks).
- Text above the tunnel: "***Distribution*** could be" (Bold Italic + Regular, ~34 px). Text below: "as important as ***innovation***". Both reveal word by word with the VO (grey → white).
- Very slow push into the tunnel. Hold through "if not more".

## Sound
A paper-tear "rip" as the face strips separate, a soft glow "shimmer" following the spotlight, a hard cut thump into the tunnel, highway rumble, and ticks for the words.

## Images — the only thing you may ask about
Before building, send one short message listing (1) a high-contrast B&W Mark Zuckerberg portrait, (2) a white truck driving at night clip, (3) the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
