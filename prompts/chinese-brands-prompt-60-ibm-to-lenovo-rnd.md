# PROMPT 60 — IBM to Lenovo RnD (broll_idea_with_logo, 9.4 s, Decoding Brands — China)

Copy everything below this line into a new chat and attach the VO clip (broll_idea_with_logo audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/UI pages, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `broll_idea_with_logo_4K_sfx.mp4` (sound effects only) and `broll_idea_with_logo_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~9.4 s).

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

Expected transcript (Whisper mishears "studied … principles"):
> …that this was not just about buying a brand for the sake of it [0.0–2.4]. Behind the scenes, Lenovo relocated entire R&D teams [2.9–6.0], they studied every single process [6.6–7.7], every design principle… [8.5–9.4]

## Beats — cream background
1. **0.0 → ~1.3 s:** the IBM logo (blue striped) sits centred and large, drifting slightly.
2. **On "buying a brand" (~1.4 s):** IBM morphs (stripe wipe) into the old blue italic "lenovo" wordmark.
3. **On "Behind the scenes" (~2.9 s):** a red "Lenovo" box logo wipes in over the old one from the left, and a small black "ThinkPad" tag pops on its top-left corner, tilted ~-30° like a stamp.
4. **~3.8 s:** the logo moves up to the top-centre and shrinks.
5. **On "relocated entire R&D teams":** card 1 slides up from the bottom, centre-right: a green-bordered rounded video card (~200 x 130 px) of a modern factory floor, with the label below it: small black italic "Relocated" over green condensed "R&D TEAMS".
6. **On "studied every single process":** card 2 appears to its left: workers in masks on a line, labelled "*Studied* / EVERY PROCESS" above it.
7. **On "every design principle":** card 3 appears on the right: a ThinkStation tower close-up, labelled "*Studied* / DESIGN PRINCIPLES" above it. The cards stay balanced around the centre. Hold.

## Sound
A soft "morph" whoosh for the logo change, a stamp thunk for the ThinkPad tag, a card slide for each card, and a light corporate pulse underneath.

## Images — the only thing you may ask about
Before building, send one short message listing (1) the IBM logo, the old lenovo wordmark, the current red Lenovo logo and the ThinkPad tag, (2) clips of a factory floor, masked workers on a line, and a ThinkStation close-up, (3) the Zero01 / Decoding Brands logos, and ask whether I'll upload them or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
