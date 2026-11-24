# PROMPT 55 — Four Point Plan Pills (peak, 9.2 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (peak audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `peak_4K_sfx.mp4` (sound effects only) and `peak_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~9.2 s).

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

Expected transcript (Whisper truncates "aggressively"):
> First, we need to act early [0.0–1.3]. Second, we need to localize aggressively [1.6–3.1]. Third, we need to move very, very fast [3.6–5.3]. And lastly, fourth, we really need to start wearing our own badge proudly [5.9–8.9].

## Look — cream background with a faint square grid (#EADFC8 lines, ~40 px)
- **Left (x ≈ 70, y ≈ 470):** a green speech-bubble badge (#13875E, ~130 x 140 px, pointer at the bottom-left) holding a flat yellow (#F2C66B) pictogram of a person. Its pose changes on each point:
  1. hand on head, thinking
  2. pointing forward
  3. arm raised, moving
  4. fist up, proud
- **Right:** four pill labels stacked (x ≈ 200, rows ~60 px apart, starting y ≈ 80). Each is a rounded rectangle with a dark-green → light-green horizontal gradient (#1F6B4E → #7FB08F), a thin dark outline and a 3 px dark offset shadow, with white Italic text (~22 px).
- Thin dashed dark curves connect the badge to each pill.

## Motion
On each number word ("First", "Second", "Third", "fourth"):
- the badge pictogram swaps pose (quick squash-pop)
- a dashed curve draws from the badge to the next pill slot
- the pill wipes open left → right with its text typing in:
  - "1. We need to act early"
  - "2. We need to localize aggressively"
  - "3. We need to move very fast"
  - "4. Wearing our own badge proudly"

Earlier pills stay. Hold with a gentle drift.

## Sound
A soft pen-scribble for the dashed curves, a UI "pop" for each pill, light typing ticks, and a confident chord on point 4.

## Images
Draw everything in code, the pictogram included. This clip needs no outside images, so don't ask me anything; just build it. (Use the Zero01 / Decoding Brands logos if they're in your files; otherwise recreate them simply.)

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
