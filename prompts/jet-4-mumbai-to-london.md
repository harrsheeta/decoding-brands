# PROMPT 4 — "Didn't stop at India → London" (Sequence_01_3, 5.4 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01_3 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame. No black border or letterbox around it.
- Design in a 1920x1080 space and render at 2x (Python + pycairo/geopandas or shapely for the map, numpy/OpenCV for compositing and glow, ffmpeg to encode).
- Deliver two files: `Sequence_01_3_4K_sfx.mp4` and `Sequence_01_3_4K_vo_sfx.mp4`.
- Length = VO length (~5.4 s).

## VO and timing
Transcribe with word timestamps (faster-whisper "small"; convert to 16 kHz mono WAV first if PyAV errors). Expected:

> And Jet Airways did not even stop at India [0.0–1.9], by 2005 [2.1–2.7] it was flying Indians [2.7–3.8] all the way to London [3.8–4.9] as well [4.9–5.4].

Use the real timestamps. Every visual change lands on a word.

## Look
- A dark tactical/HUD world map. Background near-black (#030303 edges, #18171C centre) with a dark vignette.
- Every country border drawn in thin (~0.8 px) grey lines (#5A5A66 at ~50%). Faint internal state/province lines. Tiny scattered city dots (small grey squares). Very faint lat/long grid. Slight film grain. A few subtle horizontal HUD glitch streaks near the edges, very faint.
- India: filled dark teal-grey (#1E2A30) with faint internal state lines, a crisp bright white-blue outline (#DDE6F0) and a soft glow. Use the official Survey of India border.
- Accent: red #E04848 for rings, the flight path and the plane.
- Plane: a small top-down airliner silhouette in red with a faint glow.
- Labels: Poppins/Montserrat Bold, white, small caps, connected to the point by a thin white leader line with one bend.

## Beat 1 — "Jet Airways did not even stop at India" (0.0 → ~1.9 s)
- Start close on India, slightly tilted, slowly rotating into a straight-on view. India's fill brightens from dim to lit, and its outline draws on.
- Mumbai: a small target bracket appears on the west coast.
- On "stop": a red dashed ring pulses out from Mumbai (radius grows ~4x and fades), then a second, bigger ring follows, growing past India's borders. This shows that India can't contain it.
- The camera starts pulling out (zoom out ~2x) as the rings expand.

## Beat 2 — "by 2005 it was flying Indians" (~2.1 → ~3.8 s)
- The red plane takes off from Mumbai heading north-west. A red dashed great-circle arc draws on behind it.
- The camera keeps zooming out and pans north-west to show the Middle East and Europe, with India in the bottom-right. India stays highlighted and every other country stays dim grey.
- The plane flies over Pakistan/Iran → Turkey/Black Sea → Central Europe. The camera follows, keeping the plane in the left-centre third.

## Beat 3 — "all the way to London as well" (~3.8 → end)
- The camera settles on Europe and slows to a gentle drift. The plane reaches London (south-east England) on "London".
- A small red target bracket locks onto London. A leader line extends up-right, and the label "LONDON" decodes in with a quick random-character scramble (e.g. EGQYII → LONDGT → LONDON) over ~0.4 s.
- The full dashed red arc stays visible, leaving the frame bottom-right back toward India. Hold to the end with a slow drift.

## Sound
Low dark synth drone. A sonar-like "ping" for each red ring. A short radar sweep. A jet take-off whoosh, then a sustained flight hum that fades on arrival. A digital glitch/typing chatter for the decoding label, and a soft lock-on blip at London. Keep everything under the VO.

## Images — the only thing you may ask about
Nothing here strictly needs a photo. Before building, ask me only one thing: whether I'll upload an official Survey of India India outline (SVG/GeoJSON) or you should source it. Source the world borders yourself (Natural Earth 1:10m admin-0 + admin-1). If I don't reply, source everything yourself.

## This clip overrides my saved house theme where they differ
Follow this prompt exactly: near-black background (not navy), red accent and a red dashed flight path. All intentional for this clip.

## Before delivering
Render half-scale preview stills at each beat and check: India's border correct, path geographically right (Mumbai → London great circle), label readable and not clipped, plane never leaves the frame. Fix, render 4K, mux both versions, and send them.
