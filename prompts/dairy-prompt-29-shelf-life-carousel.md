# PROMPT 29 — Shelf Life Carousel (Sequence_01_24, 10.6 s, dairy video)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01_24 audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web page, numpy/OpenCV for compositing, ffmpeg to encode).
- Deliver two files: `Sequence_01_24_4K_sfx.mp4` (sound effects only) and `Sequence_01_24_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~10.6 s).

## Style
This is my dairy video. It is not Jet Airways, Meta or the idk show, so ignore any of my saved house themes or article rules and follow ONLY the look described here, even where it differs from them.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on its word. Keep motion smooth and eased (ease-out cubic/quint, small overshoot on pops).

Expected transcript (Whisper hears the first word as "Ghee", but it's **Paneer**):
> Paneer lasts for 3–5 weeks [0.0–1.2], curd lasts for 2–4 weeks [1.9–3.2], cheese lasts for 6–9 months [3.7–5.1], butter lasts for 6–12 months [5.8–7.4] and ghee lasts for 9–12 months [8.2–9.8] and sometimes… [10.1–10.6]

## Look
- Background: near-black #111111 with a faint repeating pattern of dairy-product line icons (milk cartons, packets, bottles, tubs) in very dark grey (~6% white), tiled at a slight angle and drifting slowly.
- A horizontal carousel of rounded photo cards (radius ~18 px, soft shadow), all bottom-aligned on one baseline around y = 830.
  - The **active card** is big (~270 x 330 px), sitting left of centre.
  - The upcoming cards sit small (~140 x 180 px) in a row to its right, running off the right edge.
  - Past cards sit small to its left, sliding off the left edge.
- Label beside the active card's top-right: product name in Poppins Bold, white, ~44 px, and under it the shelf life in Poppins Light, ~24 px, light grey.

Cards, in order:
1. Paneer: white paneer cubes on a wooden board with coriander. "3–5 Weeks"
2. Curd: a red clay pot of curd, a spoon lifting some, yellow background. "2–4 Weeks"
3. Cheese: a block of yellow cheese with slices on wood. "6–9 Months"
4. Butter: a butter block on its unwrapped paper. "6–12 Months"
5. Ghee: an open orange ceramic pot of golden ghee on dark wood. "9–12 Months"

## Motion
- On each product's name in the VO, the carousel slides left (0.5 s, ease-in-out): the next card grows into the active slot while the previous one shrinks and moves left.
- The label swaps with a quick glitchy text scramble/wipe (~0.25 s).
- Start at 0.0 with Paneer already active (it scales up from small over the first 0.4 s).
- Hold on Ghee to the end.

## Sound
A soft "whoosh-click" for each carousel slide, a tiny digital tick for the label scramble, and a low warm ambient bed.

## Images — the only thing you may ask about
Before building, send one short message listing the five food photos above and ask whether I'll upload them or you should source them. If I don't reply, source them yourself (real photos, appetising, consistent lighting).

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped, the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
