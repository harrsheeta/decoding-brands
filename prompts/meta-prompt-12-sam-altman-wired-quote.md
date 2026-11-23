# PROMPT 12 — Sam Altman WIRED Quote (Sequence_02_3, 4.3 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_02_3 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web/document text, numpy/OpenCV for compositing, grain, vignette and chromatic aberration, ffmpeg to encode).
- Deliver two files: `Sequence_02_3_4K_sfx.mp4` (sound effects only) and `Sequence_02_3_4K_vo_sfx.mp4` (VO + sound effects).
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
> What Meta is doing will, in my opinion [0.0–2.3], lead to very deep cultural problems [2.4–3.9].

## Scene — light background, one shot, gentle push-in throughout (1.0 → 1.06)
- **Left:** a large B&W halftone cutout of Sam Altman (head and shoulders, speaking, a mic in the lower right of his crop), bleeding off the bottom-left of the frame. Behind him sits a solid green rectangle, offset up and left, with a thin yellow-green edge highlight on its left side.
- **Right:** the real WIRED logo (the black-and-white blocky boxed letters), centred above the quote. Behind the text, two very faint, big, light-grey slanted quotation-mark shapes.
- **Quote** (Helvetica Regular, ~44 px, black, justified, 3 lines), revealed word by word in perfect sync with the VO, each word fading from light grey to black: "What Meta is doing will, in my opinion, lead to very **deep cultural problems**." The last three words are Bold.
- 0.0–0.3: the photo, green block and logo are already settling in (a quick fade and slide from the left). Hold the full quote to the end.

## Note
This is a real Sam Altman quote reported by WIRED (2025). Keep the attribution honest: WIRED logo only, no fake source line.

## Sound
A low soft pad. A tiny soft typewriter-like tick per word (very quiet), and a subtle low accent on "deep cultural problems". Keep everything under the VO.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload a Sam Altman photo (speaking at a mic, head and shoulders) and the WIRED logo, or you should source them. If I don't reply, source them yourself (real photo only).

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or touching the frame edge, the composition balanced and centred, and every reveal landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
