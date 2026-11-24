# PROMPT 18 — Fibre Popup Glitch (Sequence_01_13, 2.36 s, idk show)

Copy everything below this line into a new chat. The reference clip is silent; attach a VO only if you have one.

---

Build a motion-graphics animation for my "idk" show. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo for the vector/isometric work, numpy/OpenCV for compositing and glow, ffmpeg to encode).
- Length: 2.36 s. The reference has no voiceover, so time every beat to the seconds given below.
- If I attach a VO with this prompt, transcribe it (faster-whisper "small" with word timestamps; convert to 16 kHz mono WAV first if PyAV errors) and retime each beat to the matching words instead, stretching the length to the VO.
- Deliver `Sequence_01_13_4K_sfx.mp4` (sound effects only), plus `Sequence_01_13_4K_vo_sfx.mp4` if I gave you a VO.

## This is my "idk" show, not the Jet Airways or Meta video
Ignore my saved Jet Airways house theme and the Meta look. This show has its own style:
- **Background:** pure black #000000. Most scenes sit on a faint isometric grid (thin #1C1C1C lines at 30°, ~120 px cells) that drifts slowly with the camera.
- **Colours:** lime green #C8FF1E (glows, fibres, highlights, coins); cash green #8EDB4F, with light-green bill faces #D8F5B8 and darker sides #5FA334; electric blue #2550FE; red #C4101A for debt; white #F2F2F2 for linework and labels; cream #EDEBDE for "real world" map scenes.
- **Type:** monospace for everything (Space Mono / IBM Plex Mono / JetBrains Mono), uppercase, wide letter-spacing for small labels (~14 px, tracking +200). Bigger labels ~28 px.
- **Illustration:** clean flat isometric (true 30° iso). Thin white outlines, solid flat fills, no gradients except a soft glow. Cash is drawn as isometric stacks of bills with a "$" seal on the top bill.
- **Watermark:** a small white bold serif "idk" sits in the top-right corner on every frame (~22 px, 50 px from the top and right edges). On light backgrounds it sits inside a small black rounded pill.
- **Motion:** crisp and snappy. Fast ease-out (expo/quint) pops with a tiny overshoot, smooth constant camera drift. No motion blur except on fast whip moves. Hard cuts between scenes unless stated.

## Beats
**0.00 → 1.30 s — retro desktop.**
- A Windows 95 desktop (teal #0E8A9A wallpaper, classic desktop icons down the left: My Computer, My Briefcase, Network Neighborhood, Inbox, Recycle Bin, The Internet, The Microsoft Network; grey taskbar at the bottom) shown on an old CRT. The screen edges bulge (barrel distortion), black shows outside the curved screen, and there are faint scanlines and slight RGB bleed.
- Centred on it, a Win95 dialog window: navy title bar reading "fibre", a close [x] box, grey body holding a picture of a fibre-optic cable with rainbow-coloured fibres fanning out, and a bevelled "buy" button.
- The camera slowly pushes in from 1.0x to 1.15x.

**1.30 → 2.00 s — popup spam.**
- The same "fibre" window duplicates rapidly. Five copies cascade diagonally down-right, each offset by ~30 px, about 0.1 s apart, with a tiny pop.
- The camera punches in harder (1.15x → 1.5x), so the stack fills the right half of the frame.

**2.00 → 2.36 s — breakdown.**
- Hard cut to a full-screen datamosh/pixel-sort glitch: big blocky pink, orange, green and white macro-blocks smearing and crawling, like a corrupted video frame. The "idk" watermark stays on top.

## Sound
A Windows-95-style error "ding" for the first popup, then a rapid stack of dings (one per copy, slightly pitched up). CRT hum and a faint whine. On the glitch: a harsh digital crunch / modem screech burst.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload a fibre-optic cable picture with rainbow fibres, or you should source or draw it. Draw the Win95 desktop and dialog yourself. If I don't reply, source or draw it yourself.

## Before delivering
Render half-scale preview stills at each beat and check: the isometric angles are consistent (true 30°), labels are crisp and not clipped, nothing overlaps unintentionally, the "idk" watermark is present on every frame, and the timing matches the beats. Fix anything wrong, then render the 4K file(s) and send them to me.
