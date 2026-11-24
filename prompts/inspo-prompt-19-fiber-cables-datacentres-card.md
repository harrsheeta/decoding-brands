# PROMPT 19 — Fiber Cables Datacentres Card (Sequence_01_14, 5.04 s, idk show)

Copy everything below this line into a new chat. The reference clip is silent; attach a VO only if you have one.

---

Build a motion-graphics animation for my "idk" show. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo for the vector/isometric work, numpy/OpenCV for compositing and glow, ffmpeg to encode).
- Length: 5.04 s. The reference has no voiceover, so time every beat to the seconds given below.
- If I attach a VO with this prompt, transcribe it (faster-whisper "small" with word timestamps; convert to 16 kHz mono WAV first if PyAV errors) and retime each beat to the matching words instead, stretching the length to the VO.
- Deliver `Sequence_01_14_4K_sfx.mp4` (sound effects only), plus `Sequence_01_14_4K_vo_sfx.mp4` if I gave you a VO.

## This is my "idk" show, not the Jet Airways or Meta video
Ignore my saved Jet Airways house theme and the Meta look. This show has its own style:
- **Background:** pure black #000000. Most scenes sit on a faint isometric grid (thin #1C1C1C lines at 30°, ~120 px cells) that drifts slowly with the camera.
- **Colours:** lime green #C8FF1E (glows, fibres, highlights, coins); cash green #8EDB4F, with light-green bill faces #D8F5B8 and darker sides #5FA334; electric blue #2550FE; red #C4101A for debt; white #F2F2F2 for linework and labels; cream #EDEBDE for "real world" map scenes.
- **Type:** monospace for everything (Space Mono / IBM Plex Mono / JetBrains Mono), uppercase, wide letter-spacing for small labels (~14 px, tracking +200). Bigger labels ~28 px.
- **Illustration:** clean flat isometric (true 30° iso). Thin white outlines, solid flat fills, no gradients except a soft glow. Cash is drawn as isometric stacks of bills with a "$" seal on the top bill.
- **Watermark:** a small white bold serif "idk" sits in the top-right corner on every frame (~22 px, 50 px from the top and right edges). On light backgrounds it sits inside a small black rounded pill.
- **Motion:** crisp and snappy. Fast ease-out (expo/quint) pops with a tiny overshoot, smooth constant camera drift. No motion blur except on fast whip moves. Hard cuts between scenes unless stated.

## Beats
A single "spec card" sits centred: a tall portrait card (~300 x 470 px) with a thin dark-grey (#2A2A2A) outer frame on black, an inner image panel, and a small widely spaced mono label under the image. Hold it still with a gentle drift.

**0.00 → 2.70 s — "FIBER CABLES".**
- Image: an extreme isometric close-up of a big white cable tube coming toward camera, with blurred dark cables and blurred lime-green cables in the background (depth of field).
- Its open end starts empty. At 0.6 s, small black inner tubes slide forward out of it.
- At 1.3 s, a glowing lime fibre slides out of the centre tube and extends.
- Label: "FIBER CABLES".

**2.70 → 3.40 s — swap.**
- The card does a quick 3D tilt-flip (rotate ~15° on Y, then swap content mid-turn) and settles.

**3.40 → 4.40 s — "DATACENTRES".**
- Image: a white isometric server rack, front panel full of drive slots with glowing lime lines and small status lights. Dark racks are blurred in the background.
- Label: "DATACENTRES".

**4.40 → 5.04 s — x-ray.**
- The rack turns into a wireframe: its outer skin fades to thin white edges, revealing a 6x6 grid of small white chips/modules arranged inside.

## Sound
A low electrical hum. A soft mechanical slide for the inner tubes, a bright "zing" for the lime fibre, a card flip whoosh, server fan whirr for the rack, and a scanner "shhk" for the x-ray. Keep it subtle.

## Images
Draw everything in code. This clip needs no outside images, so don't ask me anything; just build it.

## Before delivering
Render half-scale preview stills at each beat and check: the isometric angles are consistent (true 30°), labels are crisp and not clipped, nothing overlaps unintentionally, the "idk" watermark is present on every frame, and the timing matches the beats. Fix anything wrong, then render the 4K file(s) and send them to me.
