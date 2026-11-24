# PROMPT 39 — PD Slot Machine Reveal (jumbled_words, 2.8 s, Decoding Brands)

Copy everything below this line into a new chat and attach the VO clip (jumbled_words audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, blur and vignette, ffmpeg to encode).
- Deliver two files: `jumbled_words_4K_sfx.mp4` (sound effects only) and `jumbled_words_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~2.8 s).

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

Expected transcript:
> But then came the reveal [0.0–0.8], P&D stood for Prime… [1.4–2.6]

## ⚠ Fill this in before pasting
Second word after "D": ________ (the reference cuts at "PRIME DAC…"; write the full word here).

## Look
- Background: warm cream paper (#F8E6BF) with fine paper grain and faint specks.
- A single centred line of big letters (~110 px). "P" and "D" are fixed letters in deep green bold (#173F30, Helvetica Bold).
- Every other letter sits on its own dark tile (#1A1A1A, slightly rounded, ~90 x 110 px). Behind each tile's white letter shows a slice of a dark moody photo strip (film posters / movie stills), at ~40% opacity.

## Motion
- **0.0 → ~0.8 s ("But then came the reveal"):** "P" sits on the left. Beside it, one long dark photo strip shows big white "$" signs scrolling past like a slot machine.
- **~0.8 → ~1.4 s:** the strip splits into individual tiles, making the words "P _ _ _ _" and "D _ _ …" with gaps. Each tile keeps spinning through random characters and "$" signs (slot-machine vertical flicker).
- **From "Prime":** the tiles lock left → right into the real letters (each lock has a tiny bounce): R, I, M, E for PRIME, then the letters of the second word, finishing by the end of the clip.

## Sound
A slot-machine reel rattle under the spinning tiles, a crisp "clack" as each tile locks, and a small "ta-da" chime when PRIME completes.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the dark photo strip for the tiles (movie stills / posters) and the Zero01 Network and Decoding Brands logos, or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped (watermarks included), the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
