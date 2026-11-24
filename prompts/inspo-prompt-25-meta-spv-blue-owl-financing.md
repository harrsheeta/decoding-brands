# PROMPT 25 — Meta SPV Blue Owl Financing (Sequence_01_20, 31.72 s, idk show)

Copy everything below this line into a new chat. The reference clip is silent; attach a VO only if you have one.

---

Build a motion-graphics animation for my "idk" show. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo for the vector/isometric work, numpy/OpenCV for compositing and glow, ffmpeg to encode).
- Length: 31.72 s. The reference has no voiceover, so time every beat to the seconds given below.
- If I attach a VO with this prompt, transcribe it (faster-whisper "small" with word timestamps; convert to 16 kHz mono WAV first if PyAV errors) and retime each beat to the matching words instead, stretching the length to the VO.
- Deliver `Sequence_01_20_4K_sfx.mp4` (sound effects only), plus `Sequence_01_20_4K_vo_sfx.mp4` if I gave you a VO.

## This is my "idk" show, not the Jet Airways or Meta video
Ignore my saved Jet Airways house theme and the Meta look. This show has its own style:
- **Background:** pure black #000000. Most scenes sit on a faint isometric grid (thin #1C1C1C lines at 30°, ~120 px cells) that drifts slowly with the camera.
- **Colours:** lime green #C8FF1E (glows, fibres, highlights, coins); cash green #8EDB4F, with light-green bill faces #D8F5B8 and darker sides #5FA334; electric blue #2550FE; red #C4101A for debt; white #F2F2F2 for linework and labels; cream #EDEBDE for "real world" map scenes.
- **Type:** monospace for everything (Space Mono / IBM Plex Mono / JetBrains Mono), uppercase, wide letter-spacing for small labels (~14 px, tracking +200). Bigger labels ~28 px.
- **Illustration:** clean flat isometric (true 30° iso). Thin white outlines, solid flat fills, no gradients except a soft glow. Cash is drawn as isometric stacks of bills with a "$" seal on the top bill.
- **Watermark:** a small white bold serif "idk" sits in the top-right corner on every frame (~22 px, 50 px from the top and right edges). On light backgrounds it sits inside a small black rounded pill.
- **Motion:** crisp and snappy. Fast ease-out (expo/quint) pops with a tiny overshoot, smooth constant camera drift. No motion blur except on fast whip moves. Hard cuts between scenes unless stated.

## Beats (31.7 s — one continuous camera journey, no hard cuts)
**0.0 → 1.3 s — Meta to S.P.V.**
- A Meta icon (blue circle #2550FE with the white infinity mark) sits on the left, with a small mono label "META" under it.
- A thin white line shoots out from its right side across the frame, and the camera pans right with it.
- At the far right, a thin white outline hexagon holds "S.P.V" in white mono.

**1.3 → 4.0 s — Special Purpose Vehicle.**
- The camera centres on the hexagon, which scales up big (fills ~80% of the frame height).
- The text expands with a decode effect: "S.P.V" → "SPE PUR VEH" → "SPECIAL PURPOSE VEHICLE", the letters filling in left to right.

**4.0 → 6.0 s — the shell.**
- The hexagon shrinks and morphs into a small dark isometric cube (dark grey #1A1A1A faces, thin grey edges), centred.
- Its edges turn into a dashed white outline (an empty box).

**6.0 → 9.3 s — label.**
- A leader line pops out from the cube's top-right corner, with the label "SPV (SHELL COMPANY)" in small mono caps.

**9.3 → 10.7 s — ownership blip.**
- A small round lime icon (a hand holding a coin) pops in above the cube, pulses once, then fades.
- The label fades too.

**10.7 → 13.3 s — data centres inside.**
- The dashed cube grows bigger. Inside it, a 4x4 grid of dark isometric server-rack blocks rises up from the floor.
- At ~12.7 s, a leader label "DATA CENTERS" appears at the bottom-right.

**13.3 → 16.0 s — Meta holds the keys.**
- The camera pulls back. The Meta icon appears on the left, joined to the cube by a white line with a small key icon in a circle halfway along.
- The racks light up electric blue (top faces bright, sides darker) in a quick wave.

**16.0 → 18.0 s — Meta steps back.**
- The Meta icon and key fade to ~20%, and the racks dim back to dark grey.

**18.0 → 21.3 s — Blue Owl.**
- On the right, a "Blue Owl" icon appears: a thin white owl/bird line icon in a dark circle with a white ring, with the label "BLUE OWL".
- A line connects it to the cube, and a percentage under it counts up "0%" → "80%".
- At the same time, the dashed cube becomes a solid dark block (racks hidden inside).

**21.3 → 24.5 s — Meta's share.**
- The Meta icon returns on the left, joined to the cube's top-left with a line. Its percentage counts "0%" → "20%".
- The top 20% of the cube's height turns electric blue, a slab sitting on the dark 80% below. The two labels read META 20% / BLUE OWL 80%.

**24.5 → 27.3 s — who pays.**
- The icons fade. The cube empties to a thin outline.
- Six dashed vertical lines drop in from the top of the frame into it, and green cash bundles fall down the lines and fill the cube from the bottom, layer by layer, until it's a full cash cube.

**27.3 → 29.3 s — $27 billion.**
- A white-outlined label box "$27 BILLION" (mono) slides onto the dashed lines above the cube.
- The camera tilts upward along the lines, leaving the cube at the bottom edge.

**29.3 → 31.7 s — the lenders.**
- At the top, the dashed lines split and bend toward two logos, PIMCO (left) and BlackRock (right), in white, each with a thin underline.
- Behind them, the top of the frame fills with a lime-to-black vertical gradient (#9BE15D at the top fading to black by mid-frame), with a faint pattern of bills.
- Hold.

## Sound
Soft UI blips and line "zips" throughout. A digital decode chatter for "SPECIAL PURPOSE VEHICLE". A low hollow "box" thunk for the shell. Server hum as the racks rise and turn blue. A key "clink". Counter ticks for the percentages. A cascade of cash thuds filling the cube. A rising, airy swell on the tilt up to the lenders. A subtle low drone bed throughout.

## Images — the only thing you may ask about
Before building, send one short message listing what you need and ask whether I'll upload them or you should source them:
1. Meta logo (infinity mark)
2. Blue Owl Capital logo/icon
3. PIMCO and BlackRock logos (white versions)

If I say "source them" or don't reply, find them yourself (real logos).

## Facts
This shows Meta's Hyperion financing: a joint-venture SPV, Blue Owl owning ~80% and Meta ~20%, with ~$27B in debt placed with PIMCO and BlackRock. Keep these numbers exactly.

## Before delivering
Render half-scale preview stills at each beat and check: the isometric angles are consistent (true 30°), labels are crisp and not clipped, nothing overlaps unintentionally, the "idk" watermark is present on every frame, and the timing matches the beats. Fix anything wrong, then render the 4K file(s) and send them to me.
