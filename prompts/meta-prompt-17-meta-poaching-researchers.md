# PROMPT 17 — Meta Poaching Researchers (Sequence_02_8, 7.4 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_02_8 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/document text, numpy/OpenCV for compositing, grain, vignette and chromatic aberration, ffmpeg to encode).
- Deliver two files: `Sequence_02_8_4K_sfx.mp4` (sound effects only) and `Sequence_02_8_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~7.4 s).

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
> Meta went after the top researchers [0.0–1.4] at OpenAI [1.7], Google [2.5], Apple, etc. [3.0–3.4] with pay packages [4.2–4.8] that absolutely nobody had seen in technology [5.1–7.0].

## Scene — light grey background with a soft diagonal light gradient (white top-centre → mid grey corners)
- **0.0 → ~1.5 s:** the real Meta logo as a blue square tile (white infinity mark + "Meta") sits at left-centre. On "went after", two thin black lines shoot out from its right edge, fanning open to the right like a spotlight/funnel. The area inside the funnel brightens slightly.
- **Companies (on each name):** three white rectangular boxes with thin dark outlines stack vertically inside the funnel, on the right. Each has a small black tab label on its top edge with white bold text ("OpenAI", "Google", "Apple") and holds four Meta-green circular avatar icons (white person glyph, thin dark outline).
  - OpenAI appears on "OpenAI", Google on "Google", Apple on "Apple". Each box slides in from the right and its avatars pop in left → right.
- **"pay packages" (~4.2 s):** green dollar coins (bright green #22A83A discs, white "$", dark-green rim, soft shadow, slight 3D tilt) pop in around the boxes and inside the funnel, different sizes (60–110 px). About 3 on "pay packages", then 4–5 more on "absolutely nobody". They bob and drift gently.
- The camera drifts slowly in toward the boxes the whole time. Hold to the end.

## Sound
A soft "beam" whoosh as the funnel opens. A UI click as each company box lands and small pops for the avatars. A satisfying coin "cha-ching"/clink for the dollar coins (several, slightly varied). Light corporate pulse underneath. Keep everything under the VO.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the Meta logo or you should source it. The company names are plain text labels, so no other logos are needed. If I don't reply, source it yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or touching the frame edge, the composition balanced and centred, and every reveal landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
