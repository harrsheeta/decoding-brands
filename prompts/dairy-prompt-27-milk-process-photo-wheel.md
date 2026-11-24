# PROMPT 27 — Milk Process Photo Wheel (Sequence_01_22, 4.0 s, dairy video)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01_22 audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web page, numpy/OpenCV for compositing, ffmpeg to encode).
- Deliver two files: `Sequence_01_22_4K_sfx.mp4` (sound effects only) and `Sequence_01_22_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~4.0 s).

## Style
This is my dairy video. It is not Jet Airways, Meta or the idk show, so ignore any of my saved house themes or article rules and follow ONLY the look described here, even where it differs from them.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on its word. Keep motion smooth and eased (ease-out cubic/quint, small overshoot on pops).

Expected transcript (it starts mid-sentence):
> …basically collected from farmers [0.0–1.0], processed it [1.8–2.0], packaged it [2.5–2.8] and they deliver it [3.1–3.7].

## Look
- Background: warm light grey paper (#E8E6E0) with a very faint paper texture and soft vignette.
- A giant wheel of 4+ photo cards sits on the right. The wheel's centre is off-screen right (around x = 1500, y = 540, radius ~560 px). The cards sit along its arc, each tilted to follow the curve. Only the left arc shows, from ~11 to ~7 o'clock.
- Cards: rectangular illustrations (~360 x 300 px) with a thin off-white border and soft drop shadow, in a warm, slightly painterly illustrated style (Amul-themed). A small dark-green numbered badge (#1F4D3A circle, white number, thin white ring) sits on each card's outer-left edge.
  1. A village farmer in a blue vest handing a steel milk can to a collector in white uniform and cap
  2. A dairy plant with steel pipes and tanks and a blue "MILK PROCESSOR" sign
  3. A conveyor belt of blue-and-white Amul Taaza milk packets
  4. A blue-and-white Amul delivery truck with the Amul girl mascot painted on it
- Repeat the cards around the rest of the wheel so the arc never looks empty.
- Step label on the left (x ~120, vertically centred), Poppins Regular, ~26 px, near-black.

## Motion
- The wheel rotates counter-clockwise in steps, so each next card slides down into the 9 o'clock "active" slot, level with the label. The active card is fully bright; the others are at ~85%.
- On each step the label cross-fades: the old one fades out to light grey, the new one fades in.
  - 0.0 s: card 1 active, "Collect milk from farmers"
  - on "processed": card 2 active, "Process milk"
  - on "packaged": card 3 active, "Package milk"
  - on "deliver": card 4 active, "Deliver milk"
- Each step takes ~0.45 s with ease-in-out and a tiny settle.

## Sound
A soft mechanical "ratchet" click for each wheel step, a light paper swish, and a faint warm ambient bed.

## Images — the only thing you may ask about
Before building, send one short message listing the four card illustrations above and ask whether I'll upload them or you should create or source them. If I say "make them" or don't reply, generate them in a consistent warm illustrated style.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped, the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
