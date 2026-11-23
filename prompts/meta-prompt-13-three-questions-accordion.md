# PROMPT 13 — Three Questions Accordion (Sequence_02_4, 19.3 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_02_4 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/document text, numpy/OpenCV for compositing, grain, vignette and chromatic aberration, ffmpeg to encode).
- Deliver two files: `Sequence_02_4_4K_sfx.mp4` (sound effects only) and `Sequence_02_4_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~19.3 s).

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
> One. [0.0] How did a company with 3 billion users fall so far behind in AI in the first place? [0.9–5.2] Two. [6.1] What exactly did Mark Zuckerberg see in this 28-year-old boy that he was ready to spend 14 billion dollars because of him? [6.7–12.5] Three. [13.0] What did Meta even do to go from a joke to beating the best AI models in just one and a half years? [13.9–18.8]

## Scene — dark charcoal background, one accordion of three panels
Three tall panels sit side by side as a single centred accordion (~1400 x 680 px overall) with a thin light outline. Only one panel is expanded at a time:
- The **expanded panel** is wide, solid Meta green with a subtle halftone texture. It has a big white number top-left ("01" / "02" / "03", Helvetica Bold ~70 px), a B&W halftone photo in the upper-right area, a big white bold question word bottom-left ("HOW" / "WHAT", ~60 px), and the rest of the question in small white Helvetica to its right (2 lines).
- **Collapsed panels** are slim dark-grey (#2B2B2B) vertical tabs showing only their small number at the top.

Panel content:
- **01:** photo of Mark Zuckerberg on stage, gesturing (B&W). "**HOW** did Meta fall behind in AI despite having 3 billion users?"
- **02:** photo of Mark Zuckerberg sitting with Alexandr Wang (B&W). "**WHAT** exactly did Mark Zuckerberg see in this 28 year old boy to spend $14 billion?"
- **03:** photo of people silhouetted in front of a giant Meta logo wall (B&W). "**WHAT** did Meta even do to go from a joke to beating the best AI models?"

Motion:
- **0.0 → ~0.6 s ("One"):** all three panels appear at equal width with their photos and small labels. Then 01 expands (ease-out) while 02 and 03 compress into tabs on the right.
- **~6.0 s ("Two"):** 01 collapses into a tab on the left as 02 expands. The 02 photo wipes in from a thin vertical slit, and the number "01" slides into its tab with a quick vertical motion-blur streak.
- **~13.0 s ("Three"):** 02 collapses into the left tab stack (tabs read 01, 02) and 03 expands on the right.
- Within each panel, the photo drifts slowly (Ken Burns, ~4%). Add a slight chromatic-aberration flash during each accordion transition.

## Sound
Low tense drone throughout. A mechanical slide/clack for each accordion move. A soft low "boom" hit on each number (One / Two / Three). A subtle ticking pulse under the questions. Keep everything under the VO.

## Images — the only thing you may ask about
Before building, send one short message listing what you need and ask whether I'll upload them or you should source them:
1. Mark Zuckerberg on stage, gesturing
2. Mark Zuckerberg and Alexandr Wang together
3. People silhouetted in front of a large Meta logo wall

If I say "source them" or don't reply, find them yourself (real photos, not AI).

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or touching the frame edge, the composition balanced and centred, and every reveal landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
