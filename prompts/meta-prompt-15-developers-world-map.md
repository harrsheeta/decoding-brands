# PROMPT 15 — Developers World Map (Sequence_02_6, 8.3 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_02_6 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/document text, numpy/OpenCV for compositing, grain, vignette and chromatic aberration, ffmpeg to encode).
- Deliver two files: `Sequence_02_6_4K_sfx.mp4` (sound effects only) and `Sequence_02_6_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~8.3 s).

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
> So if developers all over the world [0.0–1.4] built over Meta's free AI [1.5–2.9], then no other company like OpenAI or Google [3.6–5.7] would get complete control of the future of AI [5.9–8.1].

## Scene — dark charcoal background
**1. "developers all over the world" (0.0 → ~1.5 s).**
- A dotted world map: the continents are made of small grey square dots (#5A5A5A at ~70%) on charcoal. Start close on Europe/Asia, slightly tilted.
- Round green avatar pins (Meta green disc, white person glyph, thin white outline) pop up across the map with small bounces.
- The camera pulls back to the whole world. Final pins (~9): western USA, eastern USA/Canada, Brazil, UK/Europe, Russia, Middle East, India, Southern Africa, Australia.

**2. "built over Meta's free AI" (~1.5 → ~3.3 s).**
- The real Meta logo on a white rounded plate appears top-centre.
- Thin white lines draw from the logo down to every pin, all at once with a slight stagger.

**3. "no other company like OpenAI or Google" (~3.5 → ~5.8 s).**
- The whole map, pins, lines and logo shrink and move into a thin white circle at centre-right, like a globe inside a ring.
- On the left, text reveals word by word (light grey → white), left-aligned: "No other / company / like OpenAI / or Google".

**4. "would get complete control of the future of AI" (~5.9 → end).**
- On the right, text reveals word by word, right-aligned: "would get / the complete / control of / the future / of AI".
- Hold the three-part composition, balanced and symmetric, to the end.

## Sound
A low digital ambience. A soft pop for each pin. A quick shimmering "connect" sweep as the lines draw. A whoosh as the map shrinks into the ring. A quiet tick per word on the text. Keep everything under the VO.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the Meta logo or you should source it. The map and pins are drawn in code. If I don't reply, source it yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or touching the frame edge, the composition balanced and centred, and every reveal landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
