# PROMPT 16 — DeepSeek Developers Moved On (Sequence_02_7, 7.3 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_02_7 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/document text, numpy/OpenCV for compositing, grain, vignette and chromatic aberration, ffmpeg to encode).
- Deliver two files: `Sequence_02_7_4K_sfx.mp4` (sound effects only) and `Sequence_02_7_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~7.3 s).

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

Expected transcript (it starts mid-sentence; the subject is DeepSeek):
> …was also free [0.0–0.6], it was cheaper to run [1.3–1.9] and probably better than Llama as well [2.1–3.9]. And just like that [4.6–5.2], many developers completely moved on [5.7–7.2].

## Scenes — dark charcoal background
**1. DeepSeek's three wins (0.0 → ~4.4 s).**
- Left: the real DeepSeek logo, a blue whale on a white square tile with a soft shadow, and the blue "deepseek" wordmark under it.
- Right: a large thin white arc (part of a big circle) cuts through the frame from top to bottom, like a dial.
- A label in a thin white outlined box (white Helvetica Bold, ~48 px) swings in along the arc, tilted, then settles level, centred right of the logo:
  - "Free" on "free"
  - "Cheaper to run" on "cheaper to run" (it swings in from the top as "Free" swings out down along the arc)
  - "Better than Llama" on "better than Llama" (same swing transition)
- The arc rotates a little with each swap, like a dial turning.

**2. "just like that, developers moved on" (~4.5 → end).**
- On "And just like that": a whip-pan left to the dotted world map from the previous clip (grey dot continents, green avatar pins, the Meta logo plate at top-left).
- The DeepSeek tile slides in from the right edge.
- On "completely moved on": the green pins lift off the map one by one and fly to the DeepSeek tile, gathering around it in a loose ring. The map and Meta logo slide out left and dim.
- Hold on DeepSeek surrounded by the pins.

## Sound
A low digital drone. A "swing" whoosh and soft click for each label. A whip-pan whoosh. A soft rising "zip" for each pin flying over, and a final settling chime. Keep everything under the VO.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload the DeepSeek and Meta logos or you should source them. If I don't reply, source them yourself.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or touching the frame edge, the composition balanced and centred, and every reveal landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
