# PROMPT 10 — Llama Researchers Left Meta (Sequence_02_1, 13.2 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_02_1 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/document text, numpy/OpenCV for compositing, grain, vignette and chromatic aberration, ffmpeg to encode).
- Deliver two files: `Sequence_02_1_4K_sfx.mp4` (sound effects only) and `Sequence_02_1_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~13.2 s).

## This is my Meta AI video, NOT the Jet Airways video
Ignore my saved Jet Airways house theme (navy, Tanker, amber, its "never" list). This video has its own look, described below. Follow it even where it breaks those old rules, e.g. on-screen text that follows the VO is intentional here.

## Meta video look (shared by every clip)
- Two kinds of background: (a) light, near-white #F4F4F4 with a heavy soft grey vignette (corners ~#7A7A7A); or (b) dark charcoal #262626 centre → #030303 edges with a strong vignette. The scene notes say which.
- Accent: Meta green #128A5E (photo blocks, highlights, avatar pins). The Meta logo keeps its real blue (#0082FB / #1AA3E8).
- Photos of people: black-and-white with a visible halftone/newsprint dot texture and a little contrast crunch, usually sitting on or in front of a solid green block.
- Type: Helvetica Neue / Neue Haas Grotesk (fallback Inter). Regular for body text, Bold for emphasis. Big numbers in Helvetica Neue Bold.
- Finish on every frame: subtle film grain, a slight RGB chromatic-aberration fringe (1–2 px) on high-contrast edges, and a soft vignette.
- Motion: eased (ease-out quint / smoothstep), with slow continuous camera drift or push. Text that follows the VO reveals word by word: each word fades from light grey to full colour exactly as it's spoken.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on a word.

Expected transcript:
> These are the 14 researchers [0.0–1.4] who built the original Llama AI model [1.5–3.3]. By then [4.3–4.4], 11 of them had already left Meta [4.8–6.2]. Things were so bad [6.8–7.3] that the company that owns Facebook [7.5–8.4], Instagram [9.1] and WhatsApp [9.9] with more than 3 billion people [10.3–11.7] using its apps every day [12.0–13.0]...

(It ends mid-sentence; that's fine.)

## Scenes — light background throughout
**1. The 14 researchers (0.0 → ~4.2 s).** A grid of 14 portrait tiles: 5 + 5 + 4, centred, the last row left-aligned. Each tile is a B&W halftone head-and-shoulders cutout on a solid green square, with the name under it in black Helvetica.
- Order: Hugo Touvron, Gautier Izacard, Xavier Martinet, Marie-Anne Lachaux, Timothée Lacroix / Thibaut Lavril, Baptiste Rozière, Naman Goyal, Eric Hambro, Faisal Azhar / Aurélien Rodriguez, Armand Joulin, Edouard Grave, Guillaume Lample. These are the real authors of the original LLaMA paper (Feb 2023).
- On "14 researchers": the tiles pop in fast, one by one in reading order (small scale overshoot, ~0.07 s apart).
- On "who built the original Llama": the camera pushes in close and pans slowly across the faces (2–3 tiles fill the frame), then pulls back out to the full grid by ~4.0 s.

**2. "11 of them had already left Meta" (~4.3 → ~6.6 s).**
- On "11": eleven portraits flip from B&W/green to a red tint (red duotone face on red square), one by one in a fast random stagger, so the count reads 11 by "left".
- The 3 who stay keep their green: Hugo Touvron, Xavier Martinet and Faisal Azhar. (Verify the real "still at Meta" three if you can; if different, use the real ones.)
- On "left Meta": the red portraits drop out of their tiles (slide down and fade), leaving empty green squares.
- Then everything collapses toward the centre into a single circle.

**3. The empire (~6.7 → ~10.2 s).**
- The circle becomes the Meta logo: a blue disc with the white infinity mark and "Meta" wordmark, thin dark outline. It spins in slightly.
- A thin black orbit ring draws around it.
- Each app icon pops onto the ring on its word: Facebook (blue disc, "f") on "Facebook", Instagram (gradient disc) on "Instagram", WhatsApp (green disc) on "WhatsApp". The icons then orbit slowly.

**4. "more than 3 billion people using its apps every day" (~10.2 → end).**
- The camera pushes in and shifts so the Meta disc sits big at left-centre, partly cropped, with the orbit and icons sweeping past.
- On the right, text reveals word by word, left-aligned on four lines:
  - "More than"
  - "**3 billion**" (big, bold)
  - "people using"
  - "its apps everyday"

## Sound
A soft click/pop per tile. A low whoosh on the push-in. A descending "error" tick for each portrait turning red, and a soft thud as they drop out. A swoosh as the grid collapses, then a warm logo "bloom". A pop for each app icon. A light rising pad under the 3 billion text. Keep everything under the VO.

## Images — the only thing you may ask about
Before building, send one short message listing what you need and ask whether I'll upload them or you should source them:
1. Headshots of the 14 LLaMA researchers listed above (real photos)
2. Meta, Facebook, Instagram and WhatsApp logos

If I say "source them" or don't reply, find them yourself (real photos only, never AI faces).

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or touching the frame edge, the composition balanced and centred, and every reveal landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
