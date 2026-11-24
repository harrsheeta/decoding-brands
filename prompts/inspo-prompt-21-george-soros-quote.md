# PROMPT 21 — George Soros Quote (Sequence_01_16, 8.52 s, idk show)

Copy everything below this line into a new chat. The reference clip is silent; attach a VO only if you have one.

---

Build a motion-graphics animation for my "idk" show. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo for the vector/isometric work, numpy/OpenCV for compositing and glow, ffmpeg to encode).
- Length: 8.52 s. The reference has no voiceover, so time every beat to the seconds given below.
- If I attach a VO with this prompt, transcribe it (faster-whisper "small" with word timestamps; convert to 16 kHz mono WAV first if PyAV errors) and retime each beat to the matching words instead, stretching the length to the VO.
- Deliver `Sequence_01_16_4K_sfx.mp4` (sound effects only), plus `Sequence_01_16_4K_vo_sfx.mp4` if I gave you a VO.

## This is my "idk" show, not the Jet Airways or Meta video
Ignore my saved Jet Airways house theme and the Meta look. This show has its own style:
- **Background:** pure black #000000. Most scenes sit on a faint isometric grid (thin #1C1C1C lines at 30°, ~120 px cells) that drifts slowly with the camera.
- **Colours:** lime green #C8FF1E (glows, fibres, highlights, coins); cash green #8EDB4F, with light-green bill faces #D8F5B8 and darker sides #5FA334; electric blue #2550FE; red #C4101A for debt; white #F2F2F2 for linework and labels; cream #EDEBDE for "real world" map scenes.
- **Type:** monospace for everything (Space Mono / IBM Plex Mono / JetBrains Mono), uppercase, wide letter-spacing for small labels (~14 px, tracking +200). Bigger labels ~28 px.
- **Illustration:** clean flat isometric (true 30° iso). Thin white outlines, solid flat fills, no gradients except a soft glow. Cash is drawn as isometric stacks of bills with a "$" seal on the top bill.
- **Watermark:** a small white bold serif "idk" sits in the top-right corner on every frame (~22 px, 50 px from the top and right edges). On light backgrounds it sits inside a small black rounded pill.
- **Motion:** crisp and snappy. Fast ease-out (expo/quint) pops with a tiny overshoot, smooth constant camera drift. No motion blur except on fast whip moves. Hard cuts between scenes unless stated.

## Beats
The background here is near-black #0E0E12 (no grid).

**0.00 → 1.20 s — portrait.**
- A B&W photo of George Soros (head and shoulders, smiling slightly) sits on a solid electric-blue square (#2550FE), with a darker navy offset shadow block behind it (8 px down-right).
- A small mono label "GEORGE SOROS" sits above the top-left corner.
- It's centred at first, then slides left to make room (ease-out), ending at about x = 22% of the frame.

**1.20 → 8.00 s — the quote types on.**
- Right of the photo, a pair of blue slanted quote marks appears (two short italic strokes, blue).
- Beneath them, the quote types on like a typewriter, one character at a time with a blinking block cursor. Courier-style mono, uppercase, off-white, ~22 px, left-aligned, wrapping at ~360 px wide.
- Text: **"BUBBLES DON'T GROW OUT OF THIN AIR... THEY HAVE A SOLID BASIS IN REALITY, IT'S JUST DISTORTED BY A MISCONCEPTION."**
- Type at a steady pace so the final full stop lands at ~8.0 s, with a short pause after "AIR...".

**8.00 → 8.52 s.** Hold. The cursor blinks twice and disappears.

## Sound
A soft typewriter key click per character, with a carriage-return "ding" at each line wrap. A faint low room tone.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload a George Soros photo (head and shoulders) or you should source it. If I don't reply, source it yourself (real photo).

## Before delivering
Render half-scale preview stills at each beat and check: the isometric angles are consistent (true 30°), labels are crisp and not clipped, nothing overlaps unintentionally, the "idk" watermark is present on every frame, and the timing matches the beats. Fix anything wrong, then render the 4K file(s) and send them to me.
