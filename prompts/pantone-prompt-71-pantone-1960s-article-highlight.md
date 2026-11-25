# PROMPT 71 — Pantone 1960s Article Highlight (article_animation, 4.9 s, Pantone episode)

Copy everything below this line into a new chat and attach the VO clip (article_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/article page, numpy/OpenCV for compositing, blur and glow, ffmpeg to encode).
- Deliver two files: `article_animation_4K_sfx.mp4` (sound effects only) and `article_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~4.9 s).

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

Expected transcript (it starts and ends mid-sentence):
> …[in 196]3, they went to 20 major ink manufacturers worldwide [0.0–2.9] and they offered them licensing [3.0–4.9]…

## Look — white background (#FFFFFF)
- A centred article card (~730 x 410 px at 1080p), white, with a thin dark-grey outline (#3A3A3A, 1.5 px) and a solid deep-green offset shadow (#1B7A55, ~8 px down-right).
- **Header band:** the headline centred in Bold, ~32 px, two lines: "1960s: Becoming an International Authority on Color Systems", with a thin divider line under it across the card.
- **Body, left:** a peach (#F8BC9E) image panel (~305 x 185 px) holding a Pantone swatch card: a white card with a peach chip on top and "PANTONE® / 13-1023 TCX / Peach Fuzz" in small type at the bottom.
- **Body, right** (Medium, ~22 px, left-aligned): "Herbert wrote to 21 major ink producers, describing the Pantone Matching System and offering to license them as manufacturers of the system's ten basic inks."

## Motion
- **0.0 → ~0.5 s:** the card slides in from the left with a slight fade, the shadow trailing, and settles.
- **Highlights:** warm yellow (#F9D58A, rectangular, 2 px padding) behind the text, each phrase in ONE continuous left → right sweep synced to the VO:
  - "Herbert wrote to 21 major ink producers," sweeps from ~0.6 s to ~2.8 s, wrapping onto the second line.
  - "offering to license them as manufacturers" sweeps on "they offered them licensing" (~3.5 → ~4.9 s), wrapping across lines.
- A slow push-in over the clip (1.0 → 1.04).

## Sound
A soft paper slide for the card, a marker "squeak-swish" stretched across each highlight, and a quiet room tone.

## Images
Draw everything in code, the Pantone swatch card included. This clip needs no outside images, so don't ask me anything; just build it.

## Note
The VO says "20 major ink manufacturers" and the article text says "21". Keep the article text as written.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped, the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
