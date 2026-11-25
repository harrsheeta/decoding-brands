# PROMPT 72 — Three Cards 01 02 03 (Sequence_01_1, 12.8 s, Pantone episode)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01_1 audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/article page, numpy/OpenCV for compositing, blur and glow, ffmpeg to encode).
- Deliver two files: `Sequence_01_1_4K_sfx.mp4` (sound effects only) and `Sequence_01_1_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~12.8 s).

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
> Well, Pantone actually did three very interesting things to solve for this [0.0–3.1], and this is where their real business genius starts [3.5–5.4]. The first interesting thing is that Pantone realized that a colour matching system will only work if everyone in the world uses the exact same… [6.1–12.8]

## Look — dark background
- Background: near-black with a soft lighter centre (#262626 → #0A0A0A) and a vignette.
- Cards: warm yellow (#F9CB7A) rectangles with square corners, a soft outer yellow glow (~25 px, ~40% opacity) and a faint inner lighter edge, like lit paper.
- Card numbers: black Medium Italic (~64 px) in "01 / 02 / 03" style.

## Beats
1. **"three very interesting things" (0.0 → ~2.8 s):** three tall cards (~140 x 185 px each), centred in a row with ~40 px gaps, pop in one after another on "did", "three" and "things", each with a small upward slide and glow bloom. Labels "01", "02", "03".
2. **~2.8 → ~4.0 s:** hold, with a slow push-in. The glow pulses softly.
3. **~4.0 → ~6.0 s ("this is where their real business genius starts"):** cut to my talking-head footage. If I don't provide it, keep the three cards on screen with a slow push.
4. **"The first interesting thing" (~6.1 → ~7.4 s):** back to the dark background with only card "01" at the left (x ≈ 65), popped in on "first".
5. **"Pantone realized that…" (~7.4 s → end):** card 01 stretches sideways into a wide banner card (~830 x 185 px). The "01" fades out and the banner shows:
   - left: a photo (~180 x 185 px) of a hand fanning out a Pantone Formula Guide swatch book
   - right: text (Medium, ~26 px, black), revealed word by word on the VO: "Pantone realised that a colour matching system only works *if everyone uses the same system*" (the last part in Bold Italic)
   Hold.

## Sound
A soft "card flip" pop with a warm chime for each number card, a gentle cut whoosh, a stretch/slide whoosh as card 01 widens, and soft ticks per word.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload (1) a photo of a hand fanning a Pantone Formula Guide swatch book and (2) my talking-head clip for ~4.0–6.0 s, or you should source the photo and skip the talking head. If I don't reply, do that.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped, the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
