# PROMPT 22 — Cisco Valuation vs Profit (Sequence_01_17, 5.24 s, idk show)

Copy everything below this line into a new chat. The reference clip is silent; attach a VO only if you have one.

---

Build a motion-graphics animation for my "idk" show. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo for the vector/isometric work, numpy/OpenCV for compositing and glow, ffmpeg to encode).
- Length: 5.24 s. The reference has no voiceover, so time every beat to the seconds given below.
- If I attach a VO with this prompt, transcribe it (faster-whisper "small" with word timestamps; convert to 16 kHz mono WAV first if PyAV errors) and retime each beat to the matching words instead, stretching the length to the VO.
- Deliver `Sequence_01_17_4K_sfx.mp4` (sound effects only), plus `Sequence_01_17_4K_vo_sfx.mp4` if I gave you a VO.

## This is my "idk" show, not the Jet Airways or Meta video
Ignore my saved Jet Airways house theme and the Meta look. This show has its own style:
- **Background:** pure black #000000. Most scenes sit on a faint isometric grid (thin #1C1C1C lines at 30°, ~120 px cells) that drifts slowly with the camera.
- **Colours:** lime green #C8FF1E (glows, fibres, highlights, coins); cash green #8EDB4F, with light-green bill faces #D8F5B8 and darker sides #5FA334; electric blue #2550FE; red #C4101A for debt; white #F2F2F2 for linework and labels; cream #EDEBDE for "real world" map scenes.
- **Type:** monospace for everything (Space Mono / IBM Plex Mono / JetBrains Mono), uppercase, wide letter-spacing for small labels (~14 px, tracking +200). Bigger labels ~28 px.
- **Illustration:** clean flat isometric (true 30° iso). Thin white outlines, solid flat fills, no gradients except a soft glow. Cash is drawn as isometric stacks of bills with a "$" seal on the top bill.
- **Watermark:** a small white bold serif "idk" sits in the top-right corner on every frame (~22 px, 50 px from the top and right edges). On light backgrounds it sits inside a small black rounded pill.
- **Motion:** crisp and snappy. Fast ease-out (expo/quint) pops with a tiny overshoot, smooth constant camera drift. No motion blur except on fast whip moves. Hard cuts between scenes unless stated.

## Beats
The scene sits on the black isometric grid floor.

**0.00 → 2.00 s — the router.**
- A white isometric network switch/router box (flat, wide, with a row of ports on its front edge and the blue Cisco logo printed on top) floats centred. It has a soft white glow halo under it and bobs very gently up and down.

**2.00 → 3.30 s — the valuation wall.**
- The camera pans down-left and pulls back.
- A massive isometric wall of green cash stacks fills the upper half of the frame: the stacks are stepped like a staircase, rising higher toward the top-right and running off the top edge. It feels enormous.
- Along its front-bottom edge, a white mono label is laid flat on the iso axis: "VALUATION: 100X".
- The router is now small, sitting at the bottom-left.

**3.30 → 5.24 s — profit.**
- The router morphs (a quick squash and pop) into a tiny cash stack of just two steps of bills.
- A white mono label is laid on the iso axis next to it: "PROFIT".
- Hold, with the camera still drifting slowly, so you can compare the huge wall with the tiny stack.

## Sound
A low electric hum for the router. A whoosh on the camera move. A heavy, layered "money avalanche" thud as the wall lands. A small, almost comically quiet "plip" for the profit stack.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the Cisco logo or you should source it. If I don't reply, source it yourself.

## Before delivering
Render half-scale preview stills at each beat and check: the isometric angles are consistent (true 30°), labels are crisp and not clipped, nothing overlaps unintentionally, the "idk" watermark is present on every frame, and the timing matches the beats. Fix anything wrong, then render the 4K file(s) and send them to me.
