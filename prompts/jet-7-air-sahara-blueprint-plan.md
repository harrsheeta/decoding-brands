# PROMPT 7 — "Crowded airports → buy Air Sahara → Jet + JetLite plan" (Sequence_01_11, 18.2 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01_11 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, bloom and vignette, ffmpeg to encode).
- Deliver two files: `Sequence_01_11_4K_sfx.mp4` and `Sequence_01_11_4K_vo_sfx.mp4`.
- Length = VO length (~18.2 s).

## VO and timing
Transcribe with word timestamps (faster-whisper "small"; convert to 16 kHz mono WAV first if PyAV errors). Expected:

> India's airports were so crowded [0.0–1.4] that getting a parking space for a new airplane [1.7–3.4] was very very difficult [3.5–4.6], and here was a chance [5.3–5.9] to get an entire airline in one shot [6.0–7.9], with all its planes [8.1–9.0], with all its parking spaces [9.6–10.4] and all its passengers [11.2–12.0]. So Jet would win the business person for Jet [12.5–14.5] and the family with JetLite [14.9–16.0]. Sounds like a great plan, right? [16.5–18.0]

Use the real timestamps. Every visual change lands on a word.

## Look — a live blueprint
- Background: royal blueprint navy (#162B60 centre → #091126 edges) with a faint square blueprint grid (~40 px cells, ~8% white), a thin inner frame border inset ~30 px, and a soft vignette.
- Line work: thin (~1.2 px) light-blue lines (#9FB6E0 at ~70%). New lines draw on with a small glowing "pen tip" point travelling along each line as it draws.
- Accent: amber #F2B52B (dashed selection boxes, highlights, people).
- Planes: real top-down plane renders, small, nose up, each in its own parking stand box.
- People: small solid pictograms (round head, body, legs); some carry a briefcase or a trolley bag.

## Scene 1 — "airports were so crowded … very very difficult" (0.0 → ~4.8 s)
- Blueprint lines draw on: a long terminal building (thin rectangle across the top) with small jet-bridge ticks under it, then a grid of 24 parking stand boxes (8 columns × 3 rows) below it, and a taxiway line under the grid.
- On "crowded": planes pop into every stand quickly, in a random stagger (each fades in with a tiny scale settle). Use a mix of airlines seen from above: Indian Airlines (red tail), Air India, and plain white others. Every stand is full.
- On "new airplane": a top-down Jet Airways 737 with a soft warm glow taxis in from the left along the taxiway, looking for a gap.
- On "very very difficult": it slows under the grid, pauses briefly at two full stands, then keeps rolling right. There's no space for it.

## Scene 2 — "a chance to get an entire airline in one shot" (~5.3 → ~8.0 s)
- On "chance": the camera whip-pans right (motion blur) to a fresh empty blueprint area. A second terminal draws on, with a white logo plate on its roof: the real Air Sahara logo.
- 12 stands (4 columns × 3 rows) draw on with glowing pen tips, then top-down Air Sahara 737s appear in them.
- Under the stands, a row of ~20 passenger pictograms (grey-blue, some with bags) builds left → right.
- On "in one shot": an amber dashed rectangle with small square corner handles (like a selection box in a design app) snaps around the entire Air Sahara terminal: building, planes and passengers.

## Scene 3 — "all its planes / parking spaces / passengers" (~8.1 → ~12.0 s)
- On "all its planes": the 12 planes tint warm gold, one by one in a quick wave.
- On "all its parking spaces": every stand box fills with translucent amber (~25%) and its outline turns amber.
- On "all its passengers": the passenger pictograms turn amber left → right.

## Scene 4 — "business person for Jet … family with JetLite" (~12.5 → ~16.2 s)
- On "So Jet": the camera pans down to clean blueprint space. A single horizontal ground line draws on.
- On "business person": a blueprint outline of a tail fin traces up from the ground line, then fills into the real Jet Airways tail (navy with the gold sun logo). An amber businessman pictogram with a briefcase stands to its left.
- On "family with JetLite": a second tail outline traces to the right of it and fills into the real JetLite tail (light blue with the sun logo). An amber family (man, woman, small child) appears to its right.
- Keep the two tails symmetric about the centre.

## Scene 5 — "Sounds like a great plan, right?" (~16.4 → end)
- The camera pulls far back (ease-out) to show everything in one wide blueprint layout: the crowded 24-stand terminal top-left (the Jet plane still idling on its taxiway), the amber Air Sahara terminal top-right, and the two tails with their people at bottom-centre.
- A slow, slightly smug hold to the end.

## Sound
Soft blueprint/drafting ticks and a light "pen scratch" as lines draw. Quick soft pops as planes fill the stands. A jet taxi hum for the Jet plane, with a small "denied" low blip at each full stand. A whoosh on the whip-pan. A crisp "select" click when the dashed box snaps. A rising shimmer for the three amber waves. Two soft "thunk" placements for the tails. A gentle, slightly ironic resolve chord on "right?". Low drone bed throughout. Keep everything under the VO.

## Images — the only thing you may ask about
Before building, send one short message listing what you need and ask whether I'll upload them or you should source them:
1. Top-down planes: Indian Airlines A320, Air India, a generic white airliner, Jet Airways 737, Air Sahara 737 (transparent PNGs)
2. Air Sahara logo (PNG/SVG)
3. Real tail fin images: Jet Airways (navy + gold sun) and JetLite (light blue + sun), cut out

If I say "source them" or don't reply, find them yourself (real liveries and logos, not AI-looking).

## Before delivering
Render half-scale preview stills at each beat. Check that the grids are perfectly aligned, no plane overlaps its stand edge, the logo is crisp, the final wide shot isn't cluttered, and the tails and people are centred. Fix, render 4K, mux both versions, and send them.
