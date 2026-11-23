# PROMPT 14 — 3 Billion People Grid (Sequence_02_5, 3.1 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_02_5 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/document text, numpy/OpenCV for compositing, grain, vignette and chromatic aberration, ffmpeg to encode).
- Deliver two files: `Sequence_02_5_4K_sfx.mp4` (sound effects only) and `Sequence_02_5_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~3.1 s).

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
> It had more than 3 billion people [0.0–1.4] using its apps every single… [1.5–3.1]

(It ends mid-sentence; that's fine.)

## Scene — warm off-white/cream background (#EBEBDF), flat, no vignette, light grain
- The real Meta logo (blue infinity mark + dark "Meta" wordmark) sits centred at the top.
- Below it, a wide grid of tiny person icons (head dot + rounded body), about 60 columns × 11 rows, evenly spaced and centred, all light warm grey (#C9C9BD). It's already on screen at 0.0 s (a quick fade-in over 0.2 s).
- On "more than": icons inside the grid start flipping to Meta green (#128A5E) to spell **"+3 Billion"** in a dot-matrix style (each letter ~5–7 icons tall), revealed left → right like an LED ticker: "+" on "more", "3" on "3", then "B-i-l-l-i-o-n" through "billion people", complete by ~2.7 s. Each icon pops slightly (scale 1.0 → 1.15 → 1.0) as it turns green.
- Hold to the end.

## Sound
A soft rapid digital "tick" cascade as the icons light up (like LED pixels). A subtle low swell on "billion". Keep everything under the VO.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the Meta logo or you should source it. If I don't reply, source it yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or touching the frame edge, the composition balanced and centred, and every reveal landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
