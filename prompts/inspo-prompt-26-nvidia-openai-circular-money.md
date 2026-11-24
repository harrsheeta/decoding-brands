# PROMPT 26 — Nvidia OpenAI Circular Money (Sequence_01_21, 11.48 s, idk show)

Copy everything below this line into a new chat. The reference clip is silent; attach a VO only if you have one.

---

Build a motion-graphics animation for my "idk" show. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo for the vector/isometric work, numpy/OpenCV for compositing and glow, ffmpeg to encode).
- Length: 11.48 s. The reference has no voiceover, so time every beat to the seconds given below.
- If I attach a VO with this prompt, transcribe it (faster-whisper "small" with word timestamps; convert to 16 kHz mono WAV first if PyAV errors) and retime each beat to the matching words instead, stretching the length to the VO.
- Deliver `Sequence_01_21_4K_sfx.mp4` (sound effects only), plus `Sequence_01_21_4K_vo_sfx.mp4` if I gave you a VO.

## This is my "idk" show, not the Jet Airways or Meta video
Ignore my saved Jet Airways house theme and the Meta look. This show has its own style:
- **Background:** pure black #000000. Most scenes sit on a faint isometric grid (thin #1C1C1C lines at 30°, ~120 px cells) that drifts slowly with the camera.
- **Colours:** lime green #C8FF1E (glows, fibres, highlights, coins); cash green #8EDB4F, with light-green bill faces #D8F5B8 and darker sides #5FA334; electric blue #2550FE; red #C4101A for debt; white #F2F2F2 for linework and labels; cream #EDEBDE for "real world" map scenes.
- **Type:** monospace for everything (Space Mono / IBM Plex Mono / JetBrains Mono), uppercase, wide letter-spacing for small labels (~14 px, tracking +200). Bigger labels ~28 px.
- **Illustration:** clean flat isometric (true 30° iso). Thin white outlines, solid flat fills, no gradients except a soft glow. Cash is drawn as isometric stacks of bills with a "$" seal on the top bill.
- **Watermark:** a small white bold serif "idk" sits in the top-right corner on every frame (~22 px, 50 px from the top and right edges). On light backgrounds it sits inside a small black rounded pill.
- **Motion:** crisp and snappy. Fast ease-out (expo/quint) pops with a tiny overshoot, smooth constant camera drift. No motion blur except on fast whip moves. Hard cuts between scenes unless stated.

## Beats
Nodes are dark hexagons (#111, thin grey outline) with a white logo inside and a small widely spaced mono label under them. Connections are thin dashed grey lines.

**0.00 → 1.30 s — NVIDIA → OpenAI.**
- An NVIDIA node (white NVIDIA eye logo) on the left and an OpenAI node (white OpenAI knot logo) on the right, joined by a dashed line.
- Lime coins (round, lime #C8FF1E with a dark "$") stream along the line from NVIDIA to OpenAI, 4–5 coins spaced out, and get absorbed.

**1.30 → 2.00 s.**
- The OpenAI node pulses: a larger lime-outlined hexagon flashes around it and fades.

**2.00 → 3.30 s — the triangle forms.**
- The two nodes glide into a triangle layout: OpenAI moves to the top-centre, NVIDIA to the bottom-left, and a new node, DATACENTER (white server-building icon), slides in at the bottom-right.
- A dashed arc draws from OpenAI round to DATACENTER on the right side, and another from NVIDIA up to OpenAI on the left. Together they form most of a circle.

**3.30 → 4.70 s — OpenAI → datacenter.**
- Coins flow along the right arc from OpenAI down to DATACENTER, which then pulses with the lime hexagon flash.

**4.70 → 7.50 s — the circle closes.**
- The bottom arc draws from DATACENTER to NVIDIA, completing a full dashed circle through all three nodes.
- A brief hold, with the camera drifting slowly.

**7.50 → 9.50 s — back to NVIDIA.**
- Coins flow along the bottom arc from DATACENTER to NVIDIA, which pulses with the lime hexagon flash.

**9.50 → 11.48 s — the loop keeps going.**
- A faint lime shimmer travels around the whole circle once (NVIDIA → OpenAI → DATACENTER → NVIDIA), showing the money loops. Hold.

## Sound
A soft coin "tink" for each coin, placed in stereo as it travels. A low synth "absorb" swell for each node pulse. A dashed-line draw "tick-tick". A subtle looping pulse bed that resolves at the end.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the NVIDIA and OpenAI logos (white versions) or you should source them. Draw the datacenter icon in code. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: the isometric angles are consistent (true 30°), labels are crisp and not clipped, nothing overlaps unintentionally, the "idk" watermark is present on every frame, and the timing matches the beats. Fix anything wrong, then render the 4K file(s) and send them to me.
