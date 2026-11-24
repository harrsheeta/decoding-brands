# PROMPT 24 — Project Hyperion 27B Debt (Sequence_01_19, 6.88 s, idk show)

Copy everything below this line into a new chat. The reference clip is silent; attach a VO only if you have one.

---

Build a motion-graphics animation for my "idk" show. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo for the vector/isometric work, numpy/OpenCV for compositing and glow, ffmpeg to encode).
- Length: 6.88 s. The reference has no voiceover, so time every beat to the seconds given below.
- If I attach a VO with this prompt, transcribe it (faster-whisper "small" with word timestamps; convert to 16 kHz mono WAV first if PyAV errors) and retime each beat to the matching words instead, stretching the length to the VO.
- Deliver `Sequence_01_19_4K_sfx.mp4` (sound effects only), plus `Sequence_01_19_4K_vo_sfx.mp4` if I gave you a VO.

## This is my "idk" show, not the Jet Airways or Meta video
Ignore my saved Jet Airways house theme and the Meta look. This show has its own style:
- **Background:** pure black #000000. Most scenes sit on a faint isometric grid (thin #1C1C1C lines at 30°, ~120 px cells) that drifts slowly with the camera.
- **Colours:** lime green #C8FF1E (glows, fibres, highlights, coins); cash green #8EDB4F, with light-green bill faces #D8F5B8 and darker sides #5FA334; electric blue #2550FE; red #C4101A for debt; white #F2F2F2 for linework and labels; cream #EDEBDE for "real world" map scenes.
- **Type:** monospace for everything (Space Mono / IBM Plex Mono / JetBrains Mono), uppercase, wide letter-spacing for small labels (~14 px, tracking +200). Bigger labels ~28 px.
- **Illustration:** clean flat isometric (true 30° iso). Thin white outlines, solid flat fills, no gradients except a soft glow. Cash is drawn as isometric stacks of bills with a "$" seal on the top bill.
- **Watermark:** a small white bold serif "idk" sits in the top-right corner on every frame (~22 px, 50 px from the top and right edges). On light backgrounds it sits inside a small black rounded pill.
- **Motion:** crisp and snappy. Fast ease-out (expo/quint) pops with a tiny overshoot, smooth constant camera drift. No motion blur except on fast whip moves. Hard cuts between scenes unless stated.

## Beats
**0.00 → 2.00 s — Project Hyperion (cream map).**
- Background: cream #EDEBDE with an isometric street map (slightly darker cream blocks, thin outline roads) and grey isometric trees with black shadows along the edges.
- In the middle sits a huge flat isometric data-centre building in electric blue #2550FE: a long low block with a darker blue side, rows of white rooftop HVAC units (each with two fan circles), small loading bays on its front wall, and "META" printed small on one end.
- Title top-left in black mono: "PROJECT HYPERION" (~28 px), with "LOUISIANA" in small grey caps under it.
- The camera drifts slowly right.

**2.00 → 2.70 s — money footprint.**
- Hard cut to the same view at night: black background, the map now drawn as thin dark-grey outlines with grey tree outlines.
- The building is replaced by a flat slab of cash on exactly the same footprint: neatly tiled light-green bills (top faces with "$" seals), a few bills thick, wrapped in a thin white outline box.

**2.70 → 6.00 s — "$27 BILLION".**
- A label appears top-left, "$27 BILLION ◉" (white mono, ~22 px). A thin white leader line runs from its dot down to the slab's back edge.
- Hold with a slow drift.

**6.00 → 6.88 s — it's debt.**
- The slab flips to solid dark red #C4101A with thin bright-red grid lines (the bills turn into a red ledger grid).
- A red mono tag "[DEBT]" types in under "$27 BILLION".

## Sound
Light outdoor ambience and a distant hum of cooling fans on the blue building. A low "drop" on the cut to night. A soft cash rustle as the slab forms. A tick for the label. A dark low "dun" and a quick alarm-ish blip when it turns red.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the Meta logo (for the "META" text) or you should source it. Draw the building, map and cash in code. If I don't reply, source it yourself.

## Before delivering
Render half-scale preview stills at each beat and check: the isometric angles are consistent (true 30°), labels are crisp and not clipped, nothing overlaps unintentionally, the "idk" watermark is present on every frame, and the timing matches the beats. Fix anything wrong, then render the 4K file(s) and send them to me.
