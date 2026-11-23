# PROMPT 1 — "Indian Airlines bad service" (Sequence_01, 15.7 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else: no concept approval, no style questions. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame. No black border or letterbox around it.
- Design in a 1920x1080 space and render at 2x (Python + pycairo for vector work, numpy/OpenCV for compositing, bloom and vignette, ffmpeg to encode).
- Deliver two files: `Sequence_01_4K_sfx.mp4` (sound effects only) and `Sequence_01_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~15.7 s).

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Expected transcript and approximate times (seconds):

> And since passengers had nowhere else to go [0.0–1.8], Indian Airlines had no reason to try as well [2.2–4.5]. Flights were neither regular [4.9–5.4] nor punctual [5.9–6.3], the staff was so rude [7.1–7.9] that passengers started treating it like a normal part of flying [8.2–10.9], and sometimes your luggage [11.5–12.5] took probably longer to arrive [12.8–14.2] than the flight itself [14.5–15.1].

Use the real timestamps from your transcription. Every visual change lands on a VO word.

## Look (whole clip)
- Background: deep navy radial gradient, centre ~#101B2D, edges ~#040509, with a heavy dark vignette. Tiny faint white star specks drift very slowly. Soft bloom on bright elements.
- Line art: thin (~1.5 px at 1080p) light grey-blue lines (#C8D2E0 at ~60%). Flat, clean, top-down/infographic feel.
- Accent: warm amber #F2B52B (glows, speech bubbles, delay text, flight path). Cancel red #E0443A.
- People: solid white rounded pictograms with a round head and a tapered body (no faces). Passengers have small dark-grey trolley suitcases with a yellow handle beside them.
- Motion: everything eased (ease-out quint / smoothstep). The camera moves continuously and slowly (drift, push in, tilt). Nothing snaps except split-flap flips.

## Scene 1 — "nowhere else to go / no reason to try" (0.0 → ~4.6 s)
- Top-down airport gate. One Indian Airlines aircraft (top-down view, white fuselage, red/orange tail) is parked at the top-centre gate, nose pointing down at the terminal. Faint dashed circles (aircraft stands) sit behind it, and evenly spaced jet-bridge posts with hatched square bases run along the terminal's top wall.
- The terminal is a big thin-outlined rectangle. The gate door under the plane is a small amber bar with a soft amber glow that pulses gently.
- Inside: ~60 white dots (passengers seen from above) scattered randomly. On "nowhere else to go" they drift and converge toward the one gate. By ~3.5 s they have packed into a tight orderly grid queue right under the gate door (about 7 per row, many rows running off the bottom).
- On "no reason to try" the camera slowly pushes in and down toward the plane and the queue (about 1.0x → 1.25x). The plane doesn't move.

## Scene 2 — "neither regular nor punctual" (~4.6 → ~7.0 s)
- Transition: a fast whip/tilt with motion blur, down to a hanging split-flap departures board. The board swings in at a slight 3D tilt (~5° rotation, slight perspective) and settles.
- Board: dark charcoal metal panel (#2E2E30), subtle bevel, rivets in the corners, hung from two thin cables. Header: "INDIAN AIRLINES" (white, left) and "DEPARTURES" (amber, right). Every character sits on its own dark flap tile with a horizontal split line.
- Six rows (flight no. / city / days / time / status):
  - 171 BOMBAY — MO TH — 07:25 — DELAYED
  - 208 MADRAS — TU — --:-- — CANCELED (red)
  - 245 CALCUTTA — WE SA — 08:30 — ON TIME (white)
  - 282 BANGALORE — TH — 10:45 — DELAYED
  - 319 LUCKNOW — MO FR — 11:50 — DELAYED
  - 356 HYDERABAD — SA — 13:30 — DELAYED
- DELAYED text and times are amber; CANCELED is red.
- On "regular" and "punctual" the flaps flip through random characters (real split-flap scramble, ~0.4 s per cell, staggered per row) and land on new values: times jump later, and some rows go DELAYED → CANCELED. ON TIME must flip to DELAYED here.

## Scene 3 — "staff so rude … normal part of flying" (~7.0 → ~11.4 s)
- The camera pulls back and down. The board shrinks to the top-centre of the frame and keeps flipping now and then (more CANCELED each time, times creeping later).
- Below it, a check-in desk on the left: thin white-outlined counter with a dark front panel and "CHECK-IN" in small amber monospace. Behind it, a staff pictogram with a yellow tie. To the right of the desk, a queue of 4 passenger pictograms, each with a suitcase. On the right wall, a small framed monitor showing the India map outline (this monitor is the bridge into Scene 4).
- A thin floor line runs under everyone.
- Dialogue in small rounded speech bubbles (Inter/Helvetica semibold). The passenger's bubble is light grey with dark text; the staff's bubble is amber with dark text. Each pops on with a small scale overshoot and holds ~0.8 s:
  1. Front passenger raises a hand: "Sir, where's my flight?"
  2. Staff points away dismissively: "Can't help you with that." The passenger throws both arms up.
  3. Next passenger steps up (the queue shuffles forward): "Please, any update?"
  4. Staff: "Maybe Thursday. Maybe not."
- On "normal part of flying" the passengers give up: shoulders drop, a small shrug, then they stand calmly. Show that it's routine, not drama.
- Keep limbs simple. Animate arms and lean only, no walk cycles except the short queue shuffle.

## Scene 4 — "your luggage took longer than the flight" (~11.4 → end)
- Transition: the camera pushes fast into the small wall monitor (match cut) until the India map fills the frame.
- Map: dark navy, India outline in thin light lines with a soft glow (use the official Survey of India border). Neighbouring countries faint. Labels in small light-grey monospace caps with small ring markers: DELHI (top) and BOMBAY (west coast).
- On "luggage": a top-down white plane icon (small aircraft silhouette) leaves Delhi, and the suitcase (the same trolley-bag icon) leaves Delhi too.
- The camera zooms in to frame the Gujarat/Maharashtra coast (Delhi top-right, Bombay bottom-left).
- The plane flies a smooth amber arc (solid, ~2 px) and reaches Bombay quickly. It banks and taxis slightly past the marker.
- The suitcase crawls along a separate thin dashed grey line, visibly much slower.
- A passenger pictogram appears next to Bombay, waits, then puts hands on hips (impatient) on "longer to arrive".
- On "the flight itself" the suitcase finally reaches Bombay. An amber ring pulses out from the Bombay marker. Hold to the end.

## Sound (sfx-only track; mix it under the VO in the other file)
Low navy drone bed throughout. Soft crowd murmur in Scene 1. Whoosh on each transition. Mechanical split-flap clatter on every flip. Short bubble "pop" for each speech bubble. Desk/foley ticks. Jet hum for the plane on the map. Small wheel rattle for the suitcase. Soft chime on the final ring pulse. Keep everything under the VO (VO peaks around -3 dB, SFX around -18 to -12 dB).

## Images — the only thing you may ask about
Before building, send me one short message listing the images you need and ask whether I'll upload them or you should source them:
1. Top-down Indian Airlines aircraft (white body, red/orange tail), transparent PNG
2. Top-down plain white airliner silhouette for the map
3. Official India outline (Survey of India border), SVG/GeoJSON

If I say "source them" or don't reply, find or draw them yourself. Keep the plane photo real, not AI-looking.

## This clip overrides my saved house theme where they differ
Follow this prompt exactly even where it differs from my saved Jet Airways theme. In particular, the white dots for passengers in Scene 1 and the amber flight-path line in Scene 4 are intentional here.

## Before delivering
Render half-scale preview stills at each beat and check: no overlaps, text readable, bubbles not covering faces or the board, nothing touching the frame edge. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
