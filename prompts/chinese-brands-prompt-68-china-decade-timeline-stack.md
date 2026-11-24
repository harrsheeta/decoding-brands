# PROMPT 68 — China Decade Timeline Stack (timeline_animation_brolls_stack, 9.6 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (timeline_animation_brolls_stack audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `timeline_animation_brolls_stack_4K_sfx.mp4` (sound effects only) and `timeline_animation_brolls_stack_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~9.6 s).

## Show look — "Decoding Brands" (Zero01 Network), China-brands episode
Ignore my saved Jet Airways / Meta / idk / dairy themes and any saved article rules; follow ONLY this look.
- **Watermarks on every frame:**
  - top-left: the "ZERO01⚡NETWORK" logo (small, ~22 px tall, 30 px from the edges; white on dark scenes, dark on light scenes)
  - top-right: the "DECODING BRANDS" yellow-green badge (~60 px)
- **Backgrounds** (each clip says which):
  - **Dark:** near-black #0B0B0B → #1A1A1A with a soft vignette.
  - **Cream:** #FBF4E6 with a very faint vertical line texture (thin lines ~4% darker, ~6 px apart, fading out toward the centre).
  - **White:** #FFFFFF.
  - **Desktop:** a macOS El Capitan / Yosemite sunset-mountain wallpaper.
- **Type:**
  - Neue Haas Grotesk / Helvetica Neue (fallback Inter) for body, labels and UI.
  - For big labels: a bold condensed sans (Bebas Neue / Barlow Condensed Bold) in caps, often with a small black italic "kicker" word above (e.g. *World's* / FACTORY).
- **Accent colours:** green #13875E (card borders, big labels), China red #D7262B, gold #F2B866.
- **Video cards:** rounded corners (~12 px) with a ~4 px green #13875E border on cream scenes; plain square tiles on dark scenes.
- **B-roll:** "b-roll" means short real video clips. Play them inside their cards/tiles; never use still frames when a clip is available.
- **Motion:** smooth, eased (ease-out quint, small overshoot on pops), with gentle constant camera drift. Text reveals follow the VO word by word.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on its word.

Expected transcript:
> …in just one single decade [0.0–1.1], China has completely flipped this narrative [1.8–3.5]. They have executed what is perhaps the most ambitious brand transformation that we have seen in [the] entire… [4.2–9.6]

## Beats — black background
- A thin red horizontal line (#D7262B, ~2 px) runs across the middle of the frame like a timeline track.

1. **"one single decade … flipped this narrative" (0.0 → ~4.1 s):** a timeline of b-roll tiles (~180 x 110 px, edge to edge) sits on the red line and scrolls left at a steady pace. Under each tile: a big white bold condensed year (~44 px) and a small grey italic caption:
   - 2008 — "China Begins Key Global Acquisitions" (bullet train footage)
   - 2009 — "Changing the Narrative" (workers / packages)
   - 2010 — "Making National Brands" (a busy shopping street)
   - 2012 — "The 12th 5-Year Plan" (a lab with scientists)
   - 2015 — "Catch Up" (city traffic in smog)
   - 2017 — "Global Acknowledgement of China's Rapid Growth" (a hand on a card reader)
   - 2021 — "Billions to MIC2025" (an automated factory corridor)
   - 2024 — "Leader in EV, 5G, AI, and Logistics" (humanoid robots boxing)
2. **"executed … most ambitious brand transformation" (~4.2 → ~8.0 s):** the timeline stops on 2024 and the labels fade. The tiles then stack at the centre in rapid overlapping cuts, each new tile popping on top slightly offset (~0.4 s apart): robot boxing, Chongqing at night with neon, a white robot arm, a robot in a tech hall, a factory of glowing yellow machines, a chip on a circuit board. The red line stays behind.
3. **~8.0 → ~8.9 s:** a circuit-board macro (cyan traces) grows to fill most of the frame.
4. **~8.9 s → end:** cut to a full-frame aerial top-down shot of a busy Chinese city intersection at golden hour. Hold.

## Sound
A steady ticking pulse under the scrolling timeline, a "thump" as it stops, rapid percussive hits on each stacked cut, a digital swell into the circuit macro, and city ambience on the final aerial.

## Images — the only thing you may ask about
Before building, send one short message listing the b-roll clips above (one per timeline year, plus the stack clips, the circuit macro and the aerial city shot) and the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Note
The 2015 caption is cut off in the reference. Use "Catch Up" unless I give you a different caption.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
