# PROMPT 09 — Meta Q2 2024 Most Advanced AI (Sequence_02, 5.2 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_02 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/document text, numpy/OpenCV for compositing, grain, vignette and chromatic aberration, ffmpeg to encode).
- Deliver two files: `Sequence_02_4K_sfx.mp4` (sound effects only) and `Sequence_02_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~5.2 s).

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
> Mark Zuckerberg had said [0.0–1.2] that by 2025 [1.4–2.2], Meta would build [2.4–3.1] the most advanced AI [3.2–4.3] in the industry [4.4–5.2].

## Scenes
**1. The report (0.0 → ~1.3 s), dark background.** A Meta "Q2 2024" earnings report cover floats centred at a slight angle with a soft shadow: a portrait card in Meta bright blue (#1AA3E8), the white Meta logo in the middle and "Q2 2024" under it. The camera drifts slowly toward it.

**2. The pages (~1.3 → ~2.3 s).** On "that by 2025" the cover flips open and the camera pulls back to reveal three white letter pages laid side by side. These are Mark Zuckerberg's real Q2 2024 earnings-call remarks, dense small type, tilted slightly in 3D. Use the real public text of the Q2 2024 Meta earnings call remarks.

**3. The line (~2.3 → end), light background.** Cut to an extreme close-up of the page text on near-white paper, with a heavy white vignette and shallow depth of field. All the text is pale grey (~20%) except one sentence from the real remarks: "...Llama 4, which **we're aiming to be the most advanced in the industry next year.**" Only that phrase is full black and sharp.
- On "Meta would build", the camera starts at "we're aiming to be".
- The camera tracks left → right along the sentence as the VO says "the most advanced AI", pushing in harder as it goes (~1x → 3x).
- On "industry" it lands on "industry next year." with a final push so that phrase fills the frame, the surrounding lines big, blurred and pale. Hold to the end.

## Sound
Low soft drone. A paper slide whoosh for the cover, a page flip for the reveal, a soft "focus" swell on the push-in, and a gentle low hit on "industry". Keep everything under the VO.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the Meta logo (white version) or you should source it. The pages are typeset from the real public Q2 2024 remarks; you don't need images for them. If I don't reply, source it yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or touching the frame edge, the composition balanced and centred, and every reveal landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
