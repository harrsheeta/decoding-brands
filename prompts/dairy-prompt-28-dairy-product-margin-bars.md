# PROMPT 28 — Dairy Product Margin Bars (Sequence_01_23, 7.7 s, dairy video)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01_23 audio or video).

---

Build a motion-graphics animation for my video from the attached VO. Everything you need is in this prompt. The ONLY thing you may ask me before building is about images (see "Images"). Don't ask anything else. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, Playwright for any web page, numpy/OpenCV for compositing, ffmpeg to encode).
- Deliver two files: `Sequence_01_23_4K_sfx.mp4` (sound effects only) and `Sequence_01_23_4K_vo_sfx.mp4` (VO + sound effects).
- Length = VO length (~7.7 s).

## Style
This is my dairy video. It is not Jet Airways, Meta or the idk show, so ignore any of my saved house themes or article rules and follow ONLY the look described here, even where it differs from them.

## VO and timing
Transcribe the attached VO with word timestamps (faster-whisper "small"; if PyAV throws an error, convert to 16 kHz mono WAV first). Use the real timestamps. Every visual change lands on its word. Keep motion smooth and eased (ease-out cubic/quint, small overshoot on pops).

Expected transcript (it starts mid-sentence):
> …15–20% margins [0.0–0.9], cheese can give you 25–45% margins [1.8–4.0], and things like ghee [4.9–5.4] and ice cream [5.8–6.0] can go even higher [6.3–7.0].

## Look
- Background: warm cream #FBF7EC, flat, with soft contact shadows under every object.
- **Left:** a glass 1-litre milk bottle with a metal cap and a green cow icon, printed "1 LITRE MILK" in green condensed caps. Beside it, a small rounded-rectangle tag with a thin green outline: "EARNINGS FROM SELLING MILK / **5%** / MARGIN". A dashed grey arrow points right toward the bars.
- **Right:** five product bars on a common baseline. Each has a solid colour bar, a matching colour label plate at its base (white condensed caps), the real product packshot standing in front of the bar's lower part, and a big percentage above (Oswald/Bebas-style bold condensed, in the bar's colour):

| Bar | Colour | Product | Label | Final value |
|---|---|---|---|---|
| 1 | blue #2B6CB0 | Amul Dahi cup | PACKAGED CURD | 15% |
| 2 | yellow #F2B705 | Amul Masti buttermilk bottle | BUTTERMILK | 20% |
| 3 | green #2E9E44 | Amul Cheese pack | CHEESE | 45% |
| 4 | red #D4202C | Gowardhan Ghee jar | GHEE | 50-60% |
| 5 | lime #B5D42C | Amul Vanilla Magic tub | ICE CREAM | 60-70%+ |

- The bar heights are proportional (ranges use their top value).

## Motion
- The bottle and the 5% tag are on screen from the start.
- For each product: its plate slides up from the baseline, the packshot drops in from above with a small bounce, then the bar grows up behind it while the number counts up and lands on its final value.
  - Curd and buttermilk: 0.0–1.0 s, on "15–20% margins"
  - Cheese: on "cheese"
  - Ghee: on "ghee"
  - Ice cream: on "ice cream"
- On "even higher", the ice-cream number gets a little "+" pop. Hold.

## Sound
A soft "plonk" for each packshot landing, a rising tonal whoosh with each bar, quick counter ticks, and a bright small chime on "even higher".

## Images — the only thing you may ask about
Before building, send one short message listing the packshots (milk bottle, Amul Dahi, Amul Masti buttermilk, Amul Cheese, Gowardhan Ghee, Amul Vanilla Magic ice cream; transparent PNGs) and ask whether I'll upload them or you should source them. If I don't reply, source them yourself (real products).

## Note
The VO says cheese is "25–45%". Keep the cheese bar at 45% as in the reference.

## Before delivering
Render half-scale preview stills at each beat and check: text crisp and readable, nothing overlapping or clipped, the composition balanced, and every change landing on its word. Fix anything wrong, then render the 4K files, mux both versions, and send them to me.
