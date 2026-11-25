# PROMPT 74 — Two Dead Ends (PEAKv2, 8.6 s, Decoding Brands — YouTube Premium)

Copy everything below this line into a new chat and attach the VO clip (PEAKv2 audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `PEAKv2_4K_sfx.mp4` (sound effects only) and `PEAKv2_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~8.6 s).

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

Expected transcript:
> YouTube, and thus the creators obviously, are stuck between two dead ends [0.0–3.7]. They have lost their most valuable users [4.2–5.4], and they cannot meaningfully measure the rest of them anymore [5.8–8.3].

## Look — cream background with a faint dot grid
- A thick dark-teal platform bar (#1E5E5A, ~620 x 22 px, square ends) runs horizontally just below the centre, with a soft blurred grey shadow under it (like it's floating).
- Standing on the bar: a green speech-bubble badge (#13875E, ~70 x 80 px, pointer at the bottom-left) holding a flat yellow (#F2C66B) pictogram of a person with a hand on their chin (stuck / thinking).
- Labels above the badge: "**CREATORS**" (black condensed caps, ~30 px) over "***Advertisers***" (black Bold Italic, ~32 px).
- Road signs: a yellow diamond "DEAD END" sign (#F2B33D, thin dark outline, small black text) on a thin grey post.

## Beats
1. **"YouTube" (0.0 s):** the bar, badge and "Advertisers" label are on screen, centred.
2. **"and thus the creators" (~1.3 s):** "CREATORS" types in above "Advertisers".
3. **"two dead ends" (~3.5 s):** a DEAD END sign swings into place on the bar's RIGHT end (pendulum settle).
4. **"They have lost their most valuable users" (~4.2 → ~5.6 s):** the camera pans right so the bar's right end and its sign sit centre-left, and the badge slides right next to the sign. To the right, "They've lost their most valuable users." (Bold, ~24 px, black, two lines) reveals word by word.
5. **"and they cannot meaningfully measure the rest" (~5.8 s → end):** the camera whips left (blur) to the bar's LEFT end, where a second DEAD END sign swings in. The badge turns to face it. To the left of the sign, "And they can't meaningfully measure the rest anymore!" (Bold, ~22 px, three lines) reveals word by word. The labels stay above the badge throughout. Hold.

## Sound
A soft pop for each label, a metal sign "clank" and creak for each sign, whooshes on the camera moves, ticks for the text, and a low pad.

## Images
Draw everything in code. This clip needs no outside images, so don't ask me anything; just build it (use the Zero01 / Decoding Brands logos if they're in your files, otherwise recreate them simply).

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
