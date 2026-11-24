# PROMPT 41 — Magnify Lens PD Tattoo (magnify_zoom, 4.0 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (magnify_zoom audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `magnify_zoom_4K_sfx.mp4` (sound effects only) and `magnify_zoom_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~4.0 s).

## Show look — "Decoding Brands" (Zero01 Network)
This is my Decoding Brands episode on the paparazzi economy. Ignore my saved Jet Airways / Meta / idk / dairy themes and any saved article rules; follow ONLY this look.
- **Watermarks on every frame:**
  - top-left: the "ZERO01⚡NETWORK" logo (white bold italic, small, ~22 px tall, 30 px from the edges)
  - top-right: the "DECODING BRANDS" badge (yellow-green speech-bubble sticker, ~60 px)
- **Background:** dark charcoal (#1E1E1E centre → #0C0C0C edges), with soft large blurred light blobs drifting very slowly and a soft vignette.
- **Type:** Neue Haas Grotesk / Helvetica Neue (fallback Inter), tight letter-spacing (−2%). Headlines Medium/Bold, body Regular.
  - Text colours: white #F5F5F5, or soft cream #F1EFC6 for "concept" words.
  - Accents: deep green #1F5A44 and sage #8CB5A3.
- **Photos:** warm, cinematic, slightly desaturated, with soft shadows. Archive and paparazzi photos are often black & white.
- **Text reveals:** follow the VO word by word. Each word fades from ~25% grey to full colour as it's spoken. Some reveals use a quick random-character "decode" scramble (noted per scene).
- **Motion:** smooth, eased (ease-out quint), with gentle continuous camera drift. Nothing static.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on its word.

Expected transcript (it starts mid-sentence):
> …with a tattoo on her forearm [0.0–1.0]. It had just two letters [1.8–2.5], P and D [2.8–3.8].

## Look and motion
- **0.0 → ~0.5 s:** a full-frame paparazzi photo of an actress walking (sunglasses, light-blue sleeveless top with a butterfly print, white bag on her shoulder, indoor/lobby background). Slight high-contrast flash look. Slow push-in.
- **On "tattoo":** everything outside a circle goes black, as if we're now looking through a magnifying lens or scope. The circle (~420 px diameter at first) has a soft dark inner vignette, a faint glass rim highlight and a slight barrel distortion inside. The image inside it is magnified ~1.6x.
- **"on her forearm" → "two letters":** the lens glides from her face down and across to her forearm (eased, slight overshoot), and the magnification inside increases (1.6x → 3.5x) as it travels.
- **On "P and D":** the lens settles on the forearm tattoo and does a final focus pull (blur → sharp) as the small script tattoo "PD" becomes clearly readable, centred in the lens. Hold.

## Sound
A soft lens "whirr" when the circle closes in, a mechanical focus-ring tick during the travel, and a subtle "focus lock" click on "P and D".

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the paparazzi photo of the actress (with the PD forearm tattoo clearly visible) and the Zero01 Network / Decoding Brands logos, or you should source them. If I don't reply, source the photo yourself (a real paparazzi image).

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
