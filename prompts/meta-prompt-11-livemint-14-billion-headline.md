# PROMPT 11 — Livemint 14 Billion Headline (Sequence_02_2, 4.3 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_02_2 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/document text, numpy/OpenCV for compositing, grain, vignette and chromatic aberration, ffmpeg to encode).
- Deliver two files: `Sequence_02_2_4K_sfx.mp4` (sound effects only) and `Sequence_02_2_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~4.3 s).

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
> He paid over $14 billion [0.0–1.7] in a deal [2.4–2.8] to bring a 28-year-old… [3.0–4.0]

(It ends mid-sentence; that's fine.)

## Scenes — plain white background (#FFFFFF), very light vignette
**1. The article card arrives (0.0 → ~0.6 s).** A white rectangular news card with a thin black outline, a green vertical bar on its left edge, and a curled page corner (light grey triangle) at the bottom-right. It arrives as a paper sheet: a page peels away/flips over the top (big grey page-turn shape sweeping across) and the card settles from a ~6° tilt to straight, centred.

**2. The card content.**
- The real Livemint logo, small and centred at the top.
- Headline (Helvetica Bold, ~40 px, 2 lines, left-aligned): **"Mark Zuckerberg paid $14 billion for Alexandr Wang's AI"**.
- Body (Helvetica Regular, ~20 px, justified, 6 lines): "A year after Mark Zuckerberg spent more than $14 billion to bring Alexandr Wang and a team of Scale AI engineers into Meta, the social media giant has its first proprietary frontier AI model. What it does not yet have is proof that Muse Spark can close the gap on Claude, Gemini and ChatGPT, or persuade investors that the company's aggressive AI pivot will amount to anything more than another expensive detour."
- If you can find the real Livemint article, match its exact headline and standfirst; otherwise use this text exactly.

**3. The highlight (~0.3 → ~3.0 s).** A solid green highlight bar sweeps left → right behind the headline in one continuous pass, synced to the VO. The covered text turns white as the bar passes.
- It reaches "$14" on "$14", "billion for" on "billion", and continues onto line 2, covering "Alexandr Wang's AI" by "to bring" (~3.0 s).
- The camera eases in a little (1.0 → 1.08) during the sweep. Hold to the end.

## Sound
A paper page-turn swish for the reveal. A marker swipe for the highlight, stretched across its length. Faint paper room tone. Keep everything under the VO.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the Livemint logo or you should source it. If I don't reply, source it yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or touching the frame edge, the composition balanced and centred, and every reveal landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
