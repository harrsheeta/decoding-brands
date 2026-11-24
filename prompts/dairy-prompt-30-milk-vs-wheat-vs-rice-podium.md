# PROMPT 30 — Milk vs Wheat vs Rice Podium (Creative_graph_animation, 6.9 s, dairy video)

Copy everything below this line into a new chat and attach the VO clip (Creative_graph_animation audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web page, numpy/OpenCV for compositing, ffmpeg to encode).
- Deliver two files: `Creative_graph_animation_4K_sfx.mp4` (sound effects only) and `Creative_graph_animation_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~6.9 s).

## Style
This is my dairy video. It is not Jet Airways, Meta or the idk show, so ignore any of my saved house themes or article rules and follow ONLY the look described here, even where it differs from them.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on its word. Keep motion smooth and eased (ease-out cubic/quint, small overshoot on pops).

Expected transcript (it starts mid-sentence):
> …makes it the single largest agricultural commodity in our country [0.0–3.5]. It is bigger than wheat [4.4–4.9] and it is bigger than rice [5.8–6.5].

## Look
- Page: pale cream-green #F4F4E4.
- Centred on it, a big rounded-corner frame (~1640 x 900 px, radius ~28 px) holding a soft, dreamy 3D product scene: a flat mossy grey stone podium on lush green moss and grass, ferns and leafy plants blurred at the sides, a soft pale-green misty background, gentle bokeh orbs and light dew sparkles. Bright, fresh daylight.
- Objects stand on the podium with soft contact shadows:
  - a blue-and-white "Milk" carton (milk-splash design)
  - a wooden bowl heaped with wheat grains, with a wooden scoop spilling grains
  - a small terracotta bowl of white rice
- Callouts: an elbow leader line (thin dark brown, ~1.5 px) rising from each object to a label. Big value in Poppins SemiBold dark brown (~34 px) with a small caps name under it (~13 px):
  - 20.5% / MILK
  - 4.8% / WHEAT
  - 7.6% / RICE / PADDY

## Motion
- **0.0 → ~1.3 s:** the milk carton starts tiny and far, then drops/zooms onto the podium centre with a soft bounce. Its shadow grows in.
- **On "agricultural commodity" (~1.7 s):** the leader line draws up from the carton and "20.5% MILK" fades in.
- **On "bigger than wheat":** the carton and its callout slide left. The empty wooden bowl drops in, and grains pour in to fill it (the scoop lands last). The wheat callout draws in with "4.8% WHEAT".
- **On "bigger than rice":** the rice bowl drops in on the right, and its callout draws with "7.6% RICE / PADDY".
- Throughout: a slow, gentle camera push (1.0 → 1.04) and floating bokeh.

## Sound
Soft nature ambience (birds, light breeze). A gentle "thup" as each object lands. A grain pour rustle for the wheat. A soft pen-draw tick for each callout.

## Images — the only thing you may ask about
Before building, send one short message listing (1) the mossy podium nature backdrop, (2) the milk carton, (3) the wheat bowl with scoop, (4) the rice bowl (transparent PNGs or renders), and ask whether I'll upload them or you should create or source them. If I don't reply, create or source them yourself, keeping them photoreal and in matching light.

## Numbers
Keep 20.5% / 4.8% / 7.6% exactly (share of agricultural output value).

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped, the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
