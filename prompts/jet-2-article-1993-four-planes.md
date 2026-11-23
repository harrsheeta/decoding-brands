# PROMPT 2 — "Article → 1993 → four planes" (Sequence_01_1, 8.6 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01_1 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame. No black border or letterbox around it.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for the article page, numpy/OpenCV for compositing, ffmpeg to encode).
- Deliver two files: `Sequence_01_1_4K_sfx.mp4` and `Sequence_01_1_4K_vo_sfx.mp4`.
- Length = VO length (~8.6 s).

## VO and timing
Transcribe with word timestamps (faster-whisper "small"; convert to 16 kHz mono WAV first if PyAV errors). Expected:

> But in the 1990s [0.0–1.2], India finally allowed private airlines to fly [1.5–3.6], and in 1993 [4.1–5.0], Jet Airways took off [5.3–6.4] with just four Boeing airplanes [6.5–7.9].

Use the real timestamps. Every visual change lands on a word.

## Part A — the news article (0.0 → ~4.8 s)
- Build a realistic news webpage in light mode, shown at a slight 3D angle on a soft white/grey background with a strong white vignette at the edges. Capture it with Playwright at 3–4x DPR so the text is razor sharp. Don't show a mouse cursor.
- Site: a fictional outlet, "The Newsdesk." Red square "N" logo, thin grey top utility bar ("Edition: IN · Sunday, October 25" on the left; Newsletters · e-Paper · Sign in on the right), search, a "Watch Live" pill and a red "Subscribe" pill. Nav: HOME INDIA WORLD BUSINESS (red, active) AVIATION TECH SPORTS EXPLAINERS OPINION VIDEOS.
- Breadcrumb "Home / Business / Aviation". Headline (bold, dark, 2 lines): **"How India opened its skies, and an airline took off with just four planes"**. Standfirst with a red left rule: "The end of the state's monopoly let private carriers into Indian aviation. Jet Airways began flying on 5 May 1993 with a fleet of four Boeing 737-300s." Byline: "Business Desk · New Delhi · Updated 05 May, 10:12 IST".
- Hero photo: a real Jet Airways Boeing 737 in flight against blue sky, caption "A Jet Airways Boeing 737." Right rail: "TRENDING" with 5 numbered plausible aviation/business headlines and a grey "ADVERTISEMENT" box.
- Body paragraphs (Inter or similar, ~18 px, dark grey):
  1. "For decades, Indian skies belonged to the state. Indian Airlines flew the domestic routes, Air India flew abroad, and travellers had little choice in between."
  2. "But in the 1990s, as the economy opened up, India finally allowed private airlines to fly. New carriers rushed in to claim a market the government had long kept to itself."
  3. "One of them would go on to define the decade. In 1993, Jet Airways took off with just four Boeing airplanes, leased 737-300s that began flying on 5 May."
  4. "Within a few years, it had grown into the country's largest private airline."
- Motion:
  - 0.0–1.2 s ("But in the 1990s"): the page drifts in at a slight angle, then scrolls smoothly down past the hero photo to the body.
  - On "India finally allowed private airlines to fly": the camera centres on paragraph 2. Every other line fades to ~25% opacity, and the target phrase "India finally allowed private airlines to fly" goes full black. An amber highlighter (#FFC56E, slightly translucent, rectangular, small padding) sweeps left → right across the phrase in ONE continuous pass, wrapping onto the second line. The highlight stays centred in frame.
  - On "and in 1993": scroll down to paragraph 3. Paragraph 2's highlight fades to a pale ghost. "1993" gets the same amber highlight in one quick sweep, and the camera pushes in hard toward "1993" (shallow depth-of-field blur on the rest of the text).
  - Highlights only ever move downward. Never highlight a line above a previous one.

## Part B — "1993" (~4.8 → ~5.3 s)
- Match cut: the push-in continues until the highlighted "1993" fills the screen. The page dissolves into a flat near-black charcoal background (#111111 with very fine film grain and a soft vignette).
- "1993" sits centred: large black digits (Inter Medium, ~200 px) on a solid amber block (#FFC56E).
- The block then collapses: the amber shrinks into a thin amber underline, the digits turn white, and two thin amber square brackets "[ ]" snap in on either side.

## Part C — "Jet Airways took off with just four Boeing airplanes" (~5.3 → end)
- On "Jet Airways": the brackets slide to the right and open wide (an empty bracket "slot").
- A top-down Jet Airways Boeing 737 (real top-down render: white fuselage, navy tail and engines, gold accents) flies in from the left, pulling a thin straight amber line behind it like a progress line from the left edge. It glides into the brackets, which close around it. A tiny amber label "01" fades in above the top-left bracket corner.
- On "four": three more identical planes fly in from the left on parallel amber lines, each landing in its own bracket labelled 02, 03, 04. They settle into an arrowhead/diamond formation: the lead plane (01) a little forward in the middle, the others staggered behind.
- On "Boeing airplanes": the brackets fade away, the labels shrink to tiny grey numbers on the lines, and the four planes keep drifting slowly rightward together in formation with slight independent bob. The camera eases back a touch. Hold to the end.
- Line style: amber #F2C27A, ~2 px, full opacity at the plane and fading slightly toward the left edge.

## Sound
Soft paper/page scroll and a subtle UI tick in Part A. A marker "squeak-swish" on each highlight. A low thump plus whoosh on the 1993 match cut. A bracket "click" for each bracket. A jet pass-by whoosh for each plane (the four overlapping, slightly pitched apart). A low drone bed underneath. Keep everything under the VO.

## Images — the only thing you may ask about
Before building, send one short message listing what you need and ask whether I'll upload them or you should source them:
1. Real photo of a Jet Airways Boeing 737 in flight (for the article hero)
2. Top-down Jet Airways Boeing 737 (transparent PNG)

If I say "source them" or don't reply, find them yourself (real photos, not AI-looking).

## This clip overrides my saved house theme where they differ
Follow this prompt exactly. Specifically: the article is in LIGHT mode, Part B/C use a near-black charcoal background (not navy), and the planes trail amber lines. All of this is intentional for this clip. No source credit line on screen.

## Before delivering
Render half-scale preview stills at each beat. Check that the highlight is centred, text is sharp, no overlaps, and the formation is symmetric and centred. Fix, render 4K, mux both versions, and send them.
