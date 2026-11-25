# PROMPT 73 — Three Questions Numbered (123_graphics, 19.8 s, Pantone episode)

Copy everything below this line into a new chat and attach the VO clip (123_graphics audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/article page, numpy/OpenCV for compositing, blur and glow, ffmpeg to encode).
- Deliver two files: `123_graphics_4K_sfx.mp4` (sound effects only) and `123_graphics_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~19.8 s).

## Look — Pantone episode
Ignore all my saved house themes (Jet Airways, Meta, idk, dairy, Decoding Brands) and any saved article rules. Follow ONLY the look described here.
- No watermarks or logos in the corners.
- **Palette** (pulled from Pantone swatches):
  - peach / salmon #F7B5A0 (Peach Fuzz #F8BC9E)
  - warm yellow #F9CB7A
  - sea green #4E9A7E
  - deep green #1B7A55
  - near-black #0E0E0E
  - off-white #F2F1EE
- **Type:** Neue Haas Grotesk / Helvetica Neue (fallback Inter), tight tracking (−2%). Medium for text, Bold or Bold Italic for emphasis.
- **Motion:** smooth and eased (ease-out quint), with a small overshoot on pops. Text that follows the VO reveals word by word (each word fades from ~25% to full as it's spoken).

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Whisper writes "Pantone" as "pantons"; it is **Pantone**. Use the real timestamps. Every visual change lands on its word.

Expected transcript:
> First, how did a colour become such a big problem that brands are ready to spend millions of dollars on it every single year? [0.0–6.3] Second, how did Pantone solve this problem with what is possibly one of the most simplest solutions ever? [7.2–12.2] And third, how did Pantone turn that simple solution into a monopoly that is so strong that even today nobody on the planet [can replace them]? [13.0–19.8]

## Look — light background
- Background: warm off-white (#ECEBE7) with fine paper grain. In the top-left corner, large out-of-focus Pantone swatch fans (peach, mint and coral blobs, very blurred, ~30% opacity) drift slowly.
- A thin deep-green (#1B7A55, 1.5 px) rectangular frame (~850 x 465 px) sits centred, with small L-shaped corner marks at the bottom-right and a short vertical tick at the top-right.
- Inside, near the top: a thin horizontal green rule ending in a short gradient bar (green fading to white, ~130 px).
- Three numbered rows (x ≈ 140, rows ~100 px apart). Each has a deep-green number badge (~70 px): a bold number inside an open circle stroke with a small gap, like a refresh icon.
- Question text in deep green (Medium, ~26 px, two lines) with key words in Bold:
  1. "How did **colour** become such a big problem that brands are ready to spend **millions** on it every single year?"
  2. "How did **Pantone solve** this **problem** with what is possibly one of the most simple solutions ever?"
  3. "How did they turn that simple solution into a **monopoly** so strong that even today no company on the planet can replace them?"

## Motion
- **0.0 s:** the frame and rule are already drawn (a quick 0.3 s draw-on).
- **On "First":** badge 1 pops in (its circle stroke draws around, the number fades in), and question 1 reveals word by word with the VO (each word goes from very light green-grey to full green).
- **On "Second":** badge 2 pops in at ~25% opacity, goes to full, and question 2 reveals with the VO.
- **On "third":** badge 3 and question 3 do the same.
- Earlier rows stay. Very slow push-in over the clip (1.0 → 1.03).

## Sound
A soft paper ambience, a gentle "ping" for each badge, and quiet ticks per word.

## Images
Draw everything in code; the blurred swatch fans can be simple blurred coloured shapes. This clip needs no outside images, so don't ask me anything; just build it.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped, the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
