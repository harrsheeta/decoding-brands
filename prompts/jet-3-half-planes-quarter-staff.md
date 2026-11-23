# PROMPT 3 — "Half the planes, a quarter of the staff" (Sequence_01_2, 8.0 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01_2 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame. No black border or letterbox around it.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, bloom and vignette, ffmpeg to encode).
- Deliver two files: `Sequence_01_2_4K_sfx.mp4` and `Sequence_01_2_4K_vo_sfx.mp4`.
- Length = VO length (~8.0 s).

## VO and timing
Transcribe with word timestamps (faster-whisper "small"; convert to 16 kHz mono WAV first if PyAV errors). Expected:

> And this small private airline [0.0–1.4], which had half the number of planes [1.4–3.1] and one fourth the staff [3.1–4.6] of Indian Airlines [4.8–5.4], slowly started taking away its passengers [5.4–7.9].

Use the real timestamps. Every visual change lands on a word.

## Look
- Background: navy radial gradient, centre ~#1A263C, edges ~#03080C, heavy dark vignette, soft bloom. Faint thin horizontal guide lines (~10% white) across the frame, like a blueprint/HUD grid.
- Planes: real side-view photo cutouts with soft shadows. Jet Airways 737s (navy/white with gold sun tail logo). Indian Airlines A320s (white body with red-orange tail and the IA logo).
- People: small solid white pictograms (round head, tapered body). Passengers in the last beat carry a small trolley bag.
- Brackets: thin amber corner brackets (#F2B52B, ~2 px, L-shaped corners only, not full boxes).
- Divider: a thin vertical line splits the frame into Indian Airlines (left) and Jet Airways (right), plus one thin horizontal floor line across the frame that separates passengers (above) from staff (below).

## Beat 1 — "this small private airline" (0.0 → ~1.4 s)
- A large real Jet Airways 737 photo fills the frame, banking gently left to right with slow parallax and a light motion blur.
- On "airline", the camera pulls back fast (with blur) and the plane shrinks into a row of 3 identical Jet 737s flying in a line across the top-right of the frame.

## Beat 2 — "half the number of planes" (~1.4 → ~3.1 s)
- 6 Indian Airlines A320s slide in from the left in two rows of 3 (top-left area), staggered, each with a small motion blur.
- The 3 Jet planes settle on the right in a single row level with the IA top row. Under each Jet plane, an empty dashed slot outline appears, showing the 3 "missing" planes.
- On "half": amber corner brackets open from a thin slit around the Jet row (bracket only the Jet planes).

## Beat 3 — "one fourth the staff" (~3.1 → ~4.6 s)
- Below the floor line: staff pictograms build in, row by row with a quick stagger, from small to full size.
- Left (Indian Airlines): 4 rows × 12 = 48 staff. Right (Jet): 1 row × 12 = 12 staff.
- On "fourth": the plane brackets fade, and amber brackets open around the single Jet staff row.

## Beat 4 — "of Indian Airlines" (~4.8 → ~5.4 s)
- The brackets fade. A row of passengers with trolley bags appears above the floor line on the Indian Airlines side (two short rows, white).

## Beat 5 — "slowly started taking away its passengers" (~5.4 → end)
- The passengers start walking right, one by one with staggered starts, crossing the centre divider onto the Jet side. Use a simple 2-frame walk bob and keep them all moving in the same direction.
- As each one crosses the divider it turns amber (#F2B52B). By the end most passengers are amber on the Jet side, with only a few white stragglers left behind.
- At the same time, the Indian Airlines side slowly loses focus: blur up to ~6 px and opacity down to ~60%. Do this by opacity and blur, not a dark overlay.
- Amber corner brackets reopen around the Jet planes, and a soft warm amber glow blooms behind the Jet row.
- The camera drifts slightly right toward the Jet side.

## Sound
Jet engine roar on the opening close-up that whooshes away on the pull-back. A whoosh for each Indian Airlines plane sliding in. A soft "tick" for each pictogram row building. A bracket click. Light footsteps and trolley-wheel rattle for the walking passengers, plus a soft rising chime as they turn amber. A low navy drone bed underneath. Keep everything under the VO.

## Images — the only thing you may ask about
Before building, send one short message listing what you need and ask whether I'll upload them or you should source them:
1. Real Jet Airways Boeing 737 photo, side/three-quarter view, in flight (transparent cutout)
2. Real Indian Airlines A320 side-view cutout (red-orange tail with IA logo)

If I say "source them" or don't reply, find them yourself (real photos, correct liveries for the 1990s, not AI-looking).

## Numbers check
The ratios on screen must match the VO exactly: Jet planes = half of Indian Airlines (3 vs 6), Jet staff = one fourth (12 vs 48).

## Before delivering
Render half-scale preview stills at each beat and check: no overlaps, symmetric and centred, pictograms evenly spaced, brackets only around the highlighted group. Fix, render 4K, mux both versions, and send them.
