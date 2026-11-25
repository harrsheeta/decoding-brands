# PROMPT 70 — Pantone Flywheel (flywheel_animation, 5.2 s, Pantone episode)

Copy everything below this line into a new chat and attach the VO clip (flywheel_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/article page, numpy/OpenCV for compositing, blur and glow, ffmpeg to encode).
- Deliver two files: `flywheel_animation_4K_sfx.mp4` (sound effects only) and `flywheel_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~5.2 s).

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
> The more brands use Pantone [0.0–1.4], the more inks they sell [1.5–2.6], and the more inks they sell [2.9–4.0], the more they push Pantone [4.2–5.2].

## Look — dark background
- Background: near-black with a soft lighter centre (#262626 → #0A0A0A) and a vignette.
- A huge flywheel: a ring (outer radius ~1150 px, thickness ~330 px) made of three thick curved arrow segments, each with a big flat arrowhead pointing clockwise, joined head to tail:
  - yellow #F9CB7A: "The more brands use / **Pantone**"
  - sea green #4E9A7E: "They sell more / **inks**"
  - peach #F7B5A0: "The more they push / **Pantone**"
- The wheel's centre sits well below the frame (around x = 960, y = 1500), so only the top arc shows and the active segment sits across the top-centre.
- Text sits on each segment, curved along the arc, in black: a small Medium line (~44 px) over a big Bold (Italic for "Pantone") line (~78 px).

## Motion
- **0.0 s:** the yellow segment sits at the top. Its small line is there, and "Pantone" fades in from faint to solid on "Pantone".
- **On "the more inks they sell" (~1.5 s):** the whole wheel rotates clockwise ~120° (ease-in-out, ~0.7 s, slight motion blur) so the green segment comes to the top. Its words reveal with the VO. It holds through the repeated "the more inks they sell", with the wheel drifting a few degrees.
- **On "the more they push Pantone" (~4.2 s):** another 120° rotation brings the peach segment to the top, and "**Pantone**" lands on the word. Hold.
- Keep a slow continuous clockwise creep (~2°/s) between the big turns so the wheel always feels alive.

## Sound
A heavy mechanical "flywheel" whoosh and a soft clunk for each 120° turn, a low hum that builds slightly on each cycle, and a soft tick per text word.

## Images
Draw everything in code. This clip needs no outside images, so don't ask me anything; just build it.

## Note
The reference reads "The sell more inks" (a typo). Use "They sell more inks".

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped, the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
