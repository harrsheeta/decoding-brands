# PROMPT 20 — Cash Grid Zoom Out (Sequence_01_15, 3.36 s, idk show)

Copy everything below this line into a new chat. The reference clip is silent; attach a VO only if you have one.

---

Build a motion-graphics animation for my "idk" show. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo for the vector/isometric work, numpy/OpenCV for compositing and glow, ffmpeg to encode).
- Length: 3.36 s. The reference has no voiceover, so time every beat to the seconds given below.
- If I attach a VO with this prompt, transcribe it (faster-whisper "small" with word timestamps; convert to 16 kHz mono WAV first if PyAV errors) and retime each beat to the matching words instead, stretching the length to the VO.
- Deliver `Sequence_01_15_4K_sfx.mp4` (sound effects only), plus `Sequence_01_15_4K_vo_sfx.mp4` if I gave you a VO.

## This is my "idk" show, not the Jet Airways or Meta video
Ignore my saved Jet Airways house theme and the Meta look. This show has its own style:
- **Background:** pure black #000000. Most scenes sit on a faint isometric grid (thin #1C1C1C lines at 30°, ~120 px cells) that drifts slowly with the camera.
- **Colours:** lime green #C8FF1E (glows, fibres, highlights, coins); cash green #8EDB4F, with light-green bill faces #D8F5B8 and darker sides #5FA334; electric blue #2550FE; red #C4101A for debt; white #F2F2F2 for linework and labels; cream #EDEBDE for "real world" map scenes.
- **Type:** monospace for everything (Space Mono / IBM Plex Mono / JetBrains Mono), uppercase, wide letter-spacing for small labels (~14 px, tracking +200). Bigger labels ~28 px.
- **Illustration:** clean flat isometric (true 30° iso). Thin white outlines, solid flat fills, no gradients except a soft glow. Cash is drawn as isometric stacks of bills with a "$" seal on the top bill.
- **Watermark:** a small white bold serif "idk" sits in the top-right corner on every frame (~22 px, 50 px from the top and right edges). On light backgrounds it sits inside a small black rounded pill.
- **Motion:** crisp and snappy. Fast ease-out (expo/quint) pops with a tiny overshoot, smooth constant camera drift. No motion blur except on fast whip moves. Hard cuts between scenes unless stated.

## Beats
**0.00 → 0.70 s — the grid draws.**
- Thin white grid lines (~1 px, 60% opacity) draw out from the top-left corner, making square cells of ~82 px.
- Small isometric cash bundles (a short stack of green bills seen from above at 30°) pop into cells in a random scatter as the lines reach them.

**0.70 → 1.40 s — the grid fills.**
- The grid completes as 6 columns x 4 rows, centred. The remaining empty cells fill one by one at random, so all 24 cells hold a cash bundle by 1.4 s. Each one is a tiny scale-pop.

**1.40 → 3.36 s — zoom out.**
- The camera zooms out fast (exponential, 1x → ~0.12x) and the grid keeps extending in every direction, growing to fill the whole frame with hundreds of tiny cells.
- The new cells fill with bundles in a rapid random sparkle, so the screen is dense with them by the end. Grid lines fade toward ~25% as they shrink.

## Sound
A soft paper "flick" per bundle at the start, accelerating into a dense rain of tiny ticks and cash-register shimmer as the grid explodes outward. A low rising swell under the zoom.

## Images
Draw everything in code. This clip needs no outside images, so don't ask me anything; just build it.

## Before delivering
Render half-scale preview stills at each beat and check: the isometric angles are consistent (true 30°), labels are crisp and not clipped, nothing overlaps unintentionally, the "idk" watermark is present on every frame, and the timing matches the beats. Fix anything wrong, then render the 4K file(s) and send them to me.
