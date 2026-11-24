# PROMPT 32 — Milk Producers Bars With Farmers (Graph_with_people_moving, 5.5 s, dairy video)

Copy everything below this line into a new chat and attach the VO clip (Graph_with_people_moving audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web page, numpy/OpenCV for compositing, ffmpeg to encode).
- Deliver two files: `Graph_with_people_moving_4K_sfx.mp4` (sound effects only) and `Graph_with_people_moving_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~5.5 s).

## Style
This is my dairy video. It is not Jet Airways, Meta or the idk show, so ignore any of my saved house themes or article rules and follow ONLY the look described here, even where it differs from them.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on its word. Keep motion smooth and eased (ease-out cubic/quint, small overshoot on pops).

Expected transcript (it starts mid-sentence):
> …is the largest producer of milk in the world [0.0–2.1]. We produce more than the US [2.9–4.1], more than China [4.7–5.0].

## Look
- Background: warm peach-cream #FBEBD3, flat, with very soft ground shadows.
- Bars: solid dark green #1F6B4A with a slightly darker right side (a subtle 3D block), standing on an invisible baseline around y = 960.
- Under each bar: a round flag icon and the country name (Inter SemiBold, ~16 px, dark).
- Above each bar: the value in Inter Bold (~34 px, dark green-black) with "million tonnes" under it (~14 px).
- Next to each bar stands a friendly flat cartoon farmer (clean outlines, soft shading):
  - **India:** a farmer with a moustache in a white kurta and pyjama and a white turban, holding a steel milk can. Stands to the right of the bar.
  - **United States:** a farmer in a red plaid shirt, blue overalls, green cap and boots, leaning on the bar. Stands to the right of the US bar.
  - **China:** a farmer in a red tang jacket and a conical straw hat, waving. Stands to the left of the China bar.
- Values: India 247.8, United States 102.5, China 45.4 (million tonnes), with heights to scale.

## Motion
- **0.0 → ~0.8 s:** the camera frames the right side. The India bar grows up from the baseline (ease-out), and the flag and name pop in.
- **~0.8 → ~2.0 s:** the Indian farmer walks in from the right edge (simple walk cycle) and stops beside the bar. The value "247.8 million tonnes" fades and pops in on "largest producer".
- **On "more than the US":** the camera pans left. The US bar grows, the US farmer walks in from the left, crosses to the right side of his bar and leans on it, and "102.5" pops in.
- **On "more than China":** the camera pans further left so all three bars fit, centred. The China bar grows, the Chinese farmer walks in from the left edge and waves, and "45.4" pops in.
- Hold the three-bar view to the end.

## Sound
A light upbeat percussive bed. A soft "whoomp" for each bar rising, light footsteps for each farmer walking in, a pop for each value, and a soft milk-can clink for the Indian farmer.

## Images — the only thing you may ask about
Before building, send one short message listing the three cartoon farmers (India, US, China, as described, consistent flat cartoon style, transparent PNGs, ideally with a few walk-cycle poses) and ask whether I'll upload them or you should create them. Draw the flag icons in code. If I don't reply, create the farmers yourself in one consistent style.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped, the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
