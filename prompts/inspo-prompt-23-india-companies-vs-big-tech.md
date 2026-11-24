# PROMPT 23 — India Companies vs Big Tech (Sequence_01_18, 11.44 s, idk show)

Copy everything below this line into a new chat. The reference clip is silent; attach a VO only if you have one.

---

Build a motion-graphics animation for my "idk" show. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo for the vector/isometric work, numpy/OpenCV for compositing and glow, ffmpeg to encode).
- Length: 11.44 s. The reference has no voiceover, so time every beat to the seconds given below.
- If I attach a VO with this prompt, transcribe it (faster-whisper "small" with word timestamps; convert to 16 kHz mono WAV first if PyAV errors) and retime each beat to the matching words instead, stretching the length to the VO.
- Deliver `Sequence_01_18_4K_sfx.mp4` (sound effects only), plus `Sequence_01_18_4K_vo_sfx.mp4` if I gave you a VO.

## This is my "idk" show, not the Jet Airways or Meta video
Ignore my saved Jet Airways house theme and the Meta look. This show has its own style:
- **Background:** pure black #000000. Most scenes sit on a faint isometric grid (thin #1C1C1C lines at 30°, ~120 px cells) that drifts slowly with the camera.
- **Colours:** lime green #C8FF1E (glows, fibres, highlights, coins); cash green #8EDB4F, with light-green bill faces #D8F5B8 and darker sides #5FA334; electric blue #2550FE; red #C4101A for debt; white #F2F2F2 for linework and labels; cream #EDEBDE for "real world" map scenes.
- **Type:** monospace for everything (Space Mono / IBM Plex Mono / JetBrains Mono), uppercase, wide letter-spacing for small labels (~14 px, tracking +200). Bigger labels ~28 px.
- **Illustration:** clean flat isometric (true 30° iso). Thin white outlines, solid flat fills, no gradients except a soft glow. Cash is drawn as isometric stacks of bills with a "$" seal on the top bill.
- **Watermark:** a small white bold serif "idk" sits in the top-right corner on every frame (~22 px, 50 px from the top and right edges). On light backgrounds it sits inside a small black rounded pill.
- **Motion:** crisp and snappy. Fast ease-out (expo/quint) pops with a tiny overshoot, smooth constant camera drift. No motion blur except on fast whip moves. Hard cuts between scenes unless stated.

## Beats
**0.00 → 4.50 s — Indian companies on the floor.**
- Start on the empty black isometric grid floor, with the camera drifting slowly.
- Real Indian company logos appear one by one, laid flat on the floor plane (skewed onto the iso ground, as if painted on it) and spread across the frame, each with a small pop:
  - Tata (blue)
  - Reliance
  - Aditya Birla Group
  - PNB
  - Lupin
  - Adani
  - SBI
  - ACC
  - Siemens (India)
  - DLF
  - Bajaj
  - L&T
  - Godrej
  - Piramal
  - Britannia
- Start slowly (one every ~0.5 s), then speed up so the floor is crowded with ~16 logos by 4.5 s.

**4.50 → 6.00 s — cash erupts.**
- Tall green cash-stack columns burst up from the floor at random spots, growing fast, covering the logos.
- The camera dives down into the green until the frame is full of stacked bills (top faces with "$" seals).

**6.00 → 11.44 s — the comparison.**
- Cut back to black. Two isometric cubes made of stacked cash sit side by side, each inside a thin white hexagonal outline (the cube's silhouette box).
- Above the left cube: a round India flag icon. Above the right cube: round icons for Google, Microsoft, Meta and Amazon in a row.
- The cubes build up from the floor (0.5 s). The right cube is slightly taller, with a stepped, uneven top.
- At ~7.3 s, value labels appear on the iso axis under each cube: "$5.1T" (left) and "$5.3T" (right).
- Hold with a slow drift.

## Sound
A soft stamp/pop for each logo, speeding up. A deep rumble and a "whoomph" for the cash eruption. A clean whoosh on the cut. Two firm "thunks" as the cubes land, and a subtle tick for each label.

## Images — the only thing you may ask about
Before building, send one short message listing what you need and ask whether I'll upload them or you should source them:
1. The 15 Indian company logos listed above
2. India flag icon
3. Google, Microsoft, Meta and Amazon logos

If I say "source them" or don't reply, find them yourself (real logos).

## Numbers
Keep "$5.1T" (combined value of the Indian companies) and "$5.3T" (the four US tech giants) exactly as written.

## Before delivering
Render half-scale preview stills at each beat and check: the isometric angles are consistent (true 30°), labels are crisp and not clipped, nothing overlaps unintentionally, the "idk" watermark is present on every frame, and the timing matches the beats. Fix anything wrong, then render the 4K file(s) and send them to me.
