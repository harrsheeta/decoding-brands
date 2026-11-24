# PROMPT 66 — Premium Prices Slot Logos (tile_animation, 5.8 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (tile_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `tile_animation_4K_sfx.mp4` (sound effects only) and `tile_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~5.8 s).

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
> Today, Chinese brands command premium prices [0.0–1.6] that used to be reserved exclusively for Western [2.0–3.9] and Japanese brands and products [4.3–5.5].

## Beats — white background
1. **0.0 → ~0.4 s:** a small China flag tile (~40 x 30 px) fades in at the left.
2. **"command premium prices" (~0.4 → ~1.8 s):** a red bar (#D7262B, ~180 x 36 px) wipes open right of the flag, reading "**Premium Prices**" in white Bold. A small grey photo tile (the Chinese national emblem / Great Hall) appears at its right end.
3. **The brand slot machine (~1.0 → ~3.8 s):** above and below the red bar, dark-grey logo bars (~180 x 36 px, each with a faint b-roll texture) scroll vertically like a slot machine through Chinese brands: BYD, Lenovo, Li-Ning, Anker, Xiaomi. Each one passes and briefly locks in line. The whole stack drifts up a little so the red bar sits mid-frame.
4. **"Western" (~3.9 s):** below the stack, a US flag tile appears with a yellow-orange gradient bar (#F5C57A → #F2A65A, ~210 x 64 px) reading "**Brands**" in black Bold (~34 px).
5. **"Japanese … products" (~4.5 s):** under it, a Japan flag (red disc) appears with a matching bar that types "**Products**". Hold.

## Sound
A slot-machine reel rattle under the scrolling logos, a "clunk" as each locks, a soft whoosh for each bar, and a gentle chime on "products".

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the BYD, Lenovo, Li-Ning, Anker and Xiaomi logos, the national emblem photo, and the Zero01 / Decoding Brands logos, or you should source them. Draw the flags in code. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
