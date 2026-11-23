# PROMPT 8 — "JetLite was still Air Sahara inside" (Sequence_01_12, 12.0 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01_12 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, bloom and vignette, ffmpeg to encode).
- Deliver two files: `Sequence_01_12_4K_sfx.mp4` and `Sequence_01_12_4K_vo_sfx.mp4`.
- Length = VO length (~12.0 s).

## VO and timing
Transcribe with word timestamps (faster-whisper "small"; convert to 16 kHz mono WAV first if PyAV errors). The clip starts mid-sentence. Expected:

> …prices on the outside [0.0–0.7], but on the inside [1.3–2.0] it was still the old Air Sahara [2.1–3.8] which had been a full service airline before [3.8–5.6], and it was now suddenly run by the same team that ran Jet [5.8–8.7] in the same way [8.8–9.6]. It even kept the business class [10.2–11.3] with free meals [11.5–12.0].

Use the real timestamps. Every visual change lands on a word.

## Look
- Background: navy radial gradient (centre ~#13233C, edges ~#04070C), heavy vignette, soft bloom.
- Accent: amber #F2B52B (scan line, brackets, people).
- Brackets: thin amber L-shaped corner brackets that open from a slit.
- Logos sit on white rounded cards (~12 px radius) with a soft shadow.
- People: small solid amber pictograms (round head, body, legs), some with a briefcase or trolley bag.

## Scene 1 — "…prices on the outside" (0.0 → ~1.3 s)
- A large top-down JetLite Boeing 737 (white body, light-blue tail and engines, JetLite titles) sits centred, nose pointing right. It's turned ~20° at first and slowly rotates level with a gentle drift. Soft shadow under it.

## Scene 2 — "but on the inside" (~1.3 → ~2.1 s)
- A thin vertical amber scan line (with a soft glow) appears at the left edge and sweeps across the plane.
- Everything the line passes becomes a top-down cabin cutaway. The wings, tail and engines fade away, and the fuselage turns into an open tube showing the cabin from above: two blocks of seat rows (blue seats) split by the aisle, a beige fuselage wall and a rounded nose cone. The camera pulls back slightly so the cutaway sits centred.
- A white logo card with the JetLite logo slides up under the cabin.

## Scene 3 — "still the old Air Sahara … full service airline before" (~2.1 → ~5.6 s)
- On "old Air Sahara": the logo card flips over (3D card flip on the horizontal axis) and lands showing the real Air Sahara logo.
- At the same time, the camera pushes in so the cabin fills the frame width.
- On "full service": amber corner brackets open around the front business-class rows near the nose (a few rows of wider seats). The economy section behind fades to ~35% brightness by opacity (no black overlay).

## Scene 4 — "run by the same team that ran Jet in the same way" (~5.8 → ~9.6 s)
- Cut (or quick cross-dissolve) to two top-down planes standing nose-up on a thin floor line: Jet Airways 737 on the left, JetLite 737 on the right, symmetric about the centre.
- On "same team": a team of 5 amber staff pictograms (some with briefcases or a trolley bag) appears under the Jet plane.
- On "that ran Jet": they walk together (simple walk bob) along the floor line from under Jet to under JetLite.
- On "in the same way": they stop under JetLite and amber brackets close around the group.

## Scene 5 — "kept the business class with free meals" (~10.2 → end)
- Two real photos slide in side by side, centred, hard edges, soft shadow: left, an airline business-class seat (big leather recliner by the window); right, an in-flight meal tray (full hot meal with bread roll and dessert).
- On "business class": amber brackets open around the seat photo.
- On "free meals": the brackets slide over to the meal photo. Hold to the end.

## Sound
Low drone bed. A soft jet hum on the opening plane. An electric scanner "zzzt" sweep for the amber line. A card-flip whoosh with a light snap for the logo. A bracket click. Light footsteps and a trolley rattle for the team walk. A soft whoosh as each photo slides in, and a bracket click for each bracket. Keep everything under the VO.

## Images — the only thing you may ask about
Before building, send one short message listing what you need and ask whether I'll upload them or you should source them:
1. Top-down JetLite Boeing 737 and top-down Jet Airways Boeing 737 (transparent PNGs)
2. JetLite logo and Air Sahara logo (PNG/SVG)
3. Photo of an airline business-class seat
4. Photo of an in-flight meal tray

The cabin cutaway can be drawn in code. If I say "source them" or don't reply, find them yourself (real photos and logos, not AI-looking).

## Before delivering
Render half-scale preview stills at each beat. Check that the logo card is crisp and centred under the cabin, the brackets enclose only the business-class rows, the team never overlaps a plane, and the photos are the same height and centred. Fix, render 4K, mux both versions, and send them.
