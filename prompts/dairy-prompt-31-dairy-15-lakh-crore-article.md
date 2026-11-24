# PROMPT 31 — Dairy 15 Lakh Crore Article (article_ani, 5.2 s, dairy video)

Copy everything below this line into a new chat and attach the VO clip (article_ani audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web page, numpy/OpenCV for compositing, ffmpeg to encode).
- Deliver two files: `article_ani_4K_sfx.mp4` (sound effects only) and `article_ani_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~5.2 s).

## Style
This is my dairy video. It is not Jet Airways, Meta or the idk show, so ignore any of my saved house themes or article rules and follow ONLY the look described here, even where it differs from them.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on its word. Keep motion smooth and eased (ease-out cubic/quint, small overshoot on pops).

Expected transcript:
> And even within India [0.0–0.6], the dairy industry [1.2–1.5] is worth over 15 lakh crore rupees [2.0–4.7].

## Look
- **Light mode.** A clean white news article page on a pale grey-cream background (#F0EFEA).
- Header: a thin black rule above and below the headline. Headline in Arial/Helvetica Bold, ~30 px, black: **"Reimagining Rural India: CEAH's Vision for Animal Husbandry in Viksit Bharat"**. Date under it in small grey: "April 20, 2026".
- Body: a photo on the left (Amul Taaza milk packs lined up on a store shelf), and three paragraphs on the right in Arial ~15 px, dark grey:
  1. "Despite its scale, India's animal husbandry sector often remains underestimated. Valued at nearly INR 20 lakh crore (approximately $200 billion), it contributes about 31% to the agricultural GDP. **The dairy sector alone accounts for INR 15 lakh crore—surpassing the combined economic value of staple crops such as rice, wheat, and sugarcane.** Yet, public perception continues to reduce livestock to everyday commodities—milk, eggs, or meat—without recognizing the vast economic engine behind them."
  2. "What makes India unique is its "production by masses" model. Unlike countries such as New Zealand, where large-scale farms dominate, India's strength lies in millions of smallholders managing two to four animals each. Together, they form an "army of farmers" driving the country's global leadership in milk production."
  3. "The spectrum of dairy farming in India is remarkably diverse—from large-scale operations like Bhagyalakshmi Dairy Farm in Pune with 3,500 animals, to smallholders like Mr. Rangappa, whose family depends entirely on the income from just two cows. This diversity, while a strength, also calls for a nuanced, multi-pronged policy approach. The needs of smallholder farmers and large commercial enterprises vary significantly, making one-size-fits-all strategies ineffective."
- Build the page as HTML and capture it with Playwright at 3–4x DPR so the text is razor sharp. No mouse cursor, no browser bar.

## Motion
- **0.0 → 1.2 s:** start close on the page, tilted ~-2°, with the headline at the top and the body in view. Slow drift.
- **On "the dairy industry" → "rupees" (~1.2 → ~4.0 s):** a warm yellow highlighter (#FFC94D, ~85% opacity, rectangular) sweeps left → right through the bold sentence in ONE continuous pass, wrapping across its lines and synced to the VO. It reaches "INR 15 lakh crore" as the VO says "15 lakh crore".
- **~4.2 → end:** the camera straightens and pulls back so the whole article sits as a flat card centred on the background, with a thin black border and a thick solid dark-green offset shadow (#2E6B4F, ~10 px down-right). The highlight stays visible. Hold.

## Sound
A soft paper/page ambience, a marker "squeak-swish" stretched across the highlight, and a gentle whoosh on the pull-back.

## Images — the only thing you may ask about
Before building, ask me only one thing: whether I'll upload a photo of Amul Taaza milk packs on a shelf, or you should source it. If I don't reply, source it yourself (real photo).

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped, the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
