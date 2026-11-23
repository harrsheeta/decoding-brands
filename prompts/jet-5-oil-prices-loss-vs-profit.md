# PROMPT 5 — "Oil prices → Jet loses, IndiGo profits" (Sequence_01_9, 16.8 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01_9 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, bloom and vignette, ffmpeg to encode).
- Deliver two files: `Sequence_01_9_4K_sfx.mp4` and `Sequence_01_9_4K_vo_sfx.mp4`.
- Length = VO length (~16.8 s).

## VO and timing
Transcribe with word timestamps (faster-whisper "small"; convert to 16 kHz mono WAV first if PyAV errors). Expected:

> In 2008–2009 [0.0–1.0], oil prices shot through the roof [1.5–3.0] and every airline in India [3.5–4.8] was buying the same fuel in the same country [5.1–6.9]. Now that year, Jet and JetLite together lost [7.6–9.5] almost 1000 crore rupees [9.9–11.4]. But IndiGo on the other hand [12.0–12.9], which was just 2 years old at that time [13.3–14.8], made a profit of 82 crore rupees [15.2–16.8].

Use the real timestamps. Every visual change lands on a word.

## Look
- Background: navy radial gradient, centre ~#13233C, edges ~#04070C, heavy vignette, soft bloom.
- Numbers and titles: Tanker (fallback Bebas Neue), with a very slight RGB chromatic-aberration fringe (1–2 px red/cyan offset) on the big numbers.
- Small labels: a monospace font (JetBrains Mono or similar) in grey-blue #8C9EBD.
- Colours: amber #FFC21A (oil line, loss bar, loss numbers), profit green #2ECC71, loss-label red #CC3B3B, white #EDF0F5.
- Planes: real top-down plane renders with soft drop shadows.

## Scene 1 — oil chart (0.0 → ~3.4 s)
- A rounded-corner chart frame (thin light-grey stroke) sits on the left two-thirds of the frame, with faint horizontal gridlines. Y axis: $40 / $60 / $80 / $100 (monospace, tiny). X axis: JAN 07 · APR 07 · JUL 07 · OCT 07 · JAN 08 · APR 08 · JUL 08.
- On "2008–2009": the title "2008–09" pops in top-right (white, Tanker, large).
- On "oil prices": a glowing amber line draws left → right with a soft amber area fill under it. It follows the real crude price shape: ~$55 in Jan 07, a small dip around Aug 07, ~$95 by Jan 08, then a steep climb to $147 in Jul 08. A white dot rides the line's tip.
- Beside the title: a small grey label "CRUDE OIL · PER BARREL", and below it a big amber counter that ticks up with the line: $58 → $95 → $147.
- On "through the roof": the line punches through the chart's top border. The border breaks at that point into small triangular shards that fly outward and fade, and the line's tip ends above the frame. Add a quick camera shake (2–3 px, 0.2 s).

## Scene 2 — same fuel (~3.4 → ~7.4 s)
- Quick cross-dissolve to a clean navy frame. A thin horizontal baseline runs across the middle. At its far left there's a tiny label "PROFIT" (white) just above the line and "LOSS" (red) just below.
- On "every airline in India": three top-down planes fly in from the left, nose to tail along the baseline, and stop centred: Jet Airways (navy tail, gold accents), JetLite (light-blue tail), IndiGo (white with indigo tail and engines).
- On "same fuel": small amber fuel droplets fall from the top of the frame in three columns, one stream above each plane, at an identical rhythm, and vanish as they reach the planes. This means all three pay for the same fuel. Keep it going gently until ~7.4 s.

## Scene 3 — "Jet and JetLite together lost almost 1000 crore" (~7.6 → ~11.8 s)
- The droplets stop. On "Jet and JetLite": IndiGo fades to ~40% opacity and greys out.
- On "lost": the Jet and JetLite planes tilt and sink below the baseline. A solid amber bar grows downward from the baseline behind them (the loss bar), and the two planes drop with it, tumbling slightly to rest at an angle near its bottom.
- An amber counter under the bar counts down fast: "−₹0 CR" → "−₹1,000 CR", landing on "crore rupees".
- On "rupees": thin amber corner brackets open from a slit around the loss bar and its number.

## Scene 4 — IndiGo profit (~12.0 → end)
- On "But IndiGo": IndiGo returns to full colour and opacity.
- On "just 2 years old": a subtle white glow pulses on IndiGo.
- On "made a profit": a solid green bar rises upward from the baseline under IndiGo, lifting the plane up with it. A green counter to its right counts "+₹0 CR" → "+₹82 CR" and lands exactly on "rupees" at the end.
- The loss bar and its brackets stay visible on the left so the contrast reads in one frame. Hold the final frame.

## Sound
Low navy drone bed. A rising tension riser with the oil line, a glass/plastic crack and shard tinkles when the border breaks. Jet pass-bys as the planes fly in. Soft liquid drips for the fuel droplets. A heavy downward whoosh and low thud for the loss bar, with fast counter ticks. A bright rising whoosh and a soft positive chime for the profit bar, with counter ticks. Keep everything under the VO.

## Images — the only thing you may ask about
Before building, send one short message listing what you need and ask whether I'll upload them or you should source them:
1. Top-down Jet Airways Boeing 737 (transparent PNG)
2. Top-down JetLite Boeing 737 (transparent PNG)
3. Top-down IndiGo Airbus A320 (transparent PNG)

If I say "source them" or don't reply, find them yourself (real liveries, not AI-looking).

## Numbers
Keep the figures exactly as the VO says: $147 oil peak, −₹1,000 CR for Jet + JetLite, +₹82 CR for IndiGo. No source line on screen.

## Before delivering
Render half-scale preview stills at each beat. Check that the bars sit exactly on the baseline, numbers aren't clipped, nothing overlaps (the planes may overlap their own bar, nothing else), and the frame is balanced. Fix, render 4K, mux both versions, and send them.
