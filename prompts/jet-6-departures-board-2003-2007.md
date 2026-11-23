# PROMPT 6 — "Departures board 2003 → 2007, half low-cost" (Sequence_01_10, 9.2 s)

Copy everything below this line into a new chat and attach the VO clip (Sequence_01_10 audio or video).

---

Build a motion-graphics animation for my explainer video from the attached VO. Everything you need is in this prompt. This clip needs no photos, so don't ask me anything. Build it, check it, and deliver.

## Output
- Full-frame 3840x2160, 29.97 fps (30000/1001), H.264, CRF 18, yuv420p, under 400 MB. The art fills the whole frame.
- Design in a 1920x1080 space and render at 2x (Python + pycairo, numpy/OpenCV for compositing, depth-of-field blur, bloom and vignette, ffmpeg to encode).
- Deliver two files: `Sequence_01_10_4K_sfx.mp4` and `Sequence_01_10_4K_vo_sfx.mp4`.
- Length = VO length (~9.2 s).

## VO and timing
Transcribe with word timestamps (faster-whisper "small"; convert to 16 kHz mono WAV first if PyAV errors). Whisper will probably mishear "Air Deccan" as "air decking". Expected:

> By 2007 [0.0–0.9], just four years after Air Deccan took off [1.0–2.6], almost one out of every two flights within India [3.1–5.1] was a low cost flight [5.4–6.2]. So millions of Indians started flying for the first time [7.0–9.0].

Use the real timestamps. Every visual change lands on a word.

## Look
- Setting: a dark airport terminal at night. Background navy (#1C2842 centre → #010409 edges) with a heavy vignette. Behind the board there's a blurred band of terminal ceiling lights/structure (soft grey-blue bokeh).
- The board: a big black split-flap departures board (#161920 panel, subtle bevel and soft shadow). Every character sits on its own dark flap tile (#22252C) with a thin horizontal split line. Characters are bold white monospace with wide letter-spacing (DejaVu Sans Mono Bold or similar).
- Header: "DEPARTURES" top-left (Tanker, white). Date top-right in amber flaps (#F2B52B). Column labels in tiny grey caps: TIME · FLIGHT · AIRLINE · DESTINATION · GATE.
- Each row has a small round status lamp at its far left, unlit (dark grey) by default.
- Flips: a real split-flap motion. Each tile cycles 4–8 random characters (~40 ms each, with the top half folding down) before landing. Stagger the tiles in a row left → right by ~25 ms.

## Board contents
Starting state (2003):
```
06:05  9W 301  JET AIRWAYS       DELHI      12
06:20  DN 211  AIR DECCAN        BANGALORE  04
06:40  9W 471  JET AIRWAYS       CHENNAI    09
06:55  S2 117  AIR SAHARA        DELHI      15
07:10  IC 171  INDIAN AIRLINES   KOLKATA    07
07:25  IC 433  INDIAN AIRLINES   HYDERABAD  11
07:45  9W 653  JET AIRWAYS       GOA        03
08:00  S2 221  AIR SAHARA        AHMEDABAD  14
08:15  9W 337  JET AIRWAYS       BANGALORE  10
08:30  IC 437  INDIAN AIRLINES   PUNE       06
```
Rows that flip to the 2007 state (flight code + airline change, everything else stays):
- Row 4 → SG 101 SPICEJET
- Row 6 → 6E 307 INDIGO
- Row 8 → G8 151 GO AIR
- Row 10 → DN 517 AIR DECCAN

Final low-cost rows (5 of 10, exactly "one out of every two"): rows 2, 4, 6, 8, 10.

## Beat 1 — "By 2007" (0.0 → ~1.0 s)
- Extreme close-up on the board's top-right corner. The date reads "14 NOV 2003" in big amber flaps. Below it you can see part of a large DESTINATION / GATE section (DELHI 12, BANGALORE 04, CHENNAI 09, cut off by the frame edge). Shallow depth of field, with the ceiling-light bokeh blurred behind.
- On "2007": the last two year tiles flip, 03 → 07.

## Beat 2 — "just four years after Air Deccan took off" (~1.0 → ~2.8 s)
- The camera pulls back smoothly (ease-out) to show the whole board centred in the top two-thirds of the frame, with the rows in their 2003 state.
- On "Air Deccan": row 2's lamp blinks amber once.
- At the same time, the four changing rows flip one after another (rows 4, 6, 8, 10, ~0.25 s apart) to SPICEJET, INDIGO, GO AIR, AIR DECCAN.

## Beat 3 — "one out of every two flights … low cost flight" (~3.1 → ~6.4 s)
- On "one out of every two": the five full-service rows (1, 3, 5, 7, 9) dim to ~30% opacity, one by one in a quick top-to-bottom stagger.
- The five low-cost rows stay full white, and their left status lamps light amber with a soft glow (top to bottom, on "low cost").
- The camera eases in slightly toward the board.

## Beat 4 — "millions of Indians started flying for the first time" (~7.0 → end)
- The camera tilts down. The board slides up and partly out of frame (its bottom rows stay visible at the top).
- Below it, a terminal glass wall: tall window panels lit cool blue (#2E4A8A to #1C2C5A), divided by dark mullions.
- In front of the glass, crowds of dark navy silhouette people (simple realistic body shapes, some pulling trolley bags) stream left and right in 2–3 depth layers (back layers smaller, fainter and blurrier). The crowd density builds up through the line, so the terminal fills with people.
- Hold on the busy terminal to the end.

## Sound
Terminal ambience (soft PA reverb hum, distant chatter) under everything. A crisp mechanical split-flap clatter for every flip, louder on the date flip. A soft low "power down" tick as each full-service row dims. A small warm "ding" or relay click for each amber lamp. The crowd murmur and footsteps/trolley wheels swell in Beat 4. Keep everything under the VO.

## This clip overrides my saved house theme where they differ
Follow this prompt exactly. The dark silhouette people (instead of white pictograms) are intentional here. No source line on screen.

## Before delivering
Render half-scale preview stills at each beat. Check that every character sits inside its tile, the rows are perfectly aligned, the dimmed rows are still readable but clearly secondary, and exactly 5 rows are lit. Fix, render 4K, mux both versions, and send them.
