# Prompt: "John Wick → iPhone" card animation (year timeline, then flip into a trail)

Paste this into a new chat, then attach the VO clip and the card images (posters / product shots as framed card PNGs, or plain images that you will frame).

You are my motion designer. Recreate my **"John Wick to iPhone Cards"** animation for the new VO, exactly in this style, retimed to the new words and swapped to the new subjects. A reference script is at the end: copy it, change only the beat times, images, years and counts, and keep everything else as it is.

## What the animation is
**Background:** plain charcoal, a little lighter at the top left (formula in the script), plus grain, soft bloom and vignette. Never navy, never pure black.

**Cards:**
- 3:4 cards with chamfered corners (cut = 11% of width) and a thin white/light-grey border. My PNGs usually come already framed with transparent corners, so use them as they are. If an image is not framed, crop it to 3:4 (top-biased) and frame it yourself.
- **One smooth blurred drop shadow** per card.
- No glare/shine on these cards unless I ask.

**Part 1: the year row** (e.g. three films in a series):
- Card 1 appears centred on its word: scale 0.62 → 1 with a light back-ease (s=0.9, 0.62 s) and a fade-in.
- Card 2 appears on its word the same way, 460 px to the right. The camera pans right (cubic in-out) and pulls back (zoom 1.14 → 1.07 → 1.0), so earlier cards drift left to make room.
- The same for card 3.
- Under each card its **release year** rises in, in Pricedown 58, white with a soft shadow.
- Under the years runs a **small vertical-tick timeline**:
  - Ticks every 17 px: minor 15 px, major 34 px at each card. White → light grey gradient, with a thin baseline.
  - It grows from card to card as each new card lands, with a soft glow at the growing head and a few fading lead-in ticks on the left.

**Transition** (on the word that changes subject, e.g. "Apple launches…"):
- The camera moves **up** (cubic in-out, ~0.8 s) and the first row slides down and fades out.
- At the same time the **last card** travels up-left on a slight arc and **flips** (horizontal scale = cos, swap at 90°, darken 45%·sin) into the new subject's logo card.
- Then it flips again on the product name into the **biggest card** (height 540).

**Part 2: the trail** (e.g. 10 iPhones, newest first):
- Each next card is 14% smaller (`h_i = 540·0.86^i`), slightly darker (`3.5%·i`), and overlaps the previous one by 20%. Later cards draw behind earlier ones.
- They slide out from behind the previous card one after another (0.075 s apart, ease-out quint, 0.42 s each).
- The camera pans right and pulls back to zoom ~0.86 so the whole trail fits, centred.
- Timeline under the trail with **only two years**: the newest year under the first card, the oldest under the last card.

## Files the reference script expects
`cards/<key>.png` (RGBA, 3:4, transparent chamfer corners), keys listed in `SRC`. Rename the keys/lists for new subjects: `JW_*` = part 1 row, `IKEYS` = trail (biggest first), `apple` = the logo card the last card flips into.

## Rules
- Order the cards exactly as the story needs (part 1 oldest → newest; part 2 newest → oldest).
- Verify the release years with a quick web search when they're not given.
- All text is Pricedown, white. No other fonts on screen.
- Keep everything inside the frame with margins. Check the last frame especially, since the trail is wide.

## Sound (`build_sfx.py`)
- Drone −26 dB.
- Per card in part 1: whoosh −22 + `sub_hit(80,40)` −24 + tick −30, plus a quick tick cascade (−36) while the timeline grows.
- Transition: whoosh −19, `paper` −24 at the flip, whoosh −23 + `sub_hit` −19 at the second flip.
- Trail: one rising tick per card (−29, panned left→right), a fine tick cascade (−38), and `confirm()` −27 at the end.

## Shared rules (apply to both)
- Ask me **only** for images you cannot get yourself (and for `pricedown.zip` if the Pricedown font is not installed). Everything else: decide, build, render, send.
- Pipeline from the `hash-explainer-motion-graphics` skill: faster-whisper `small` int8 word timestamps (decode to 16 kHz mono f32 and pass the array), pycairo + numpy/OpenCV, `sfx.py` (write it to `/root/sfx/sfx.py` from §8 of that skill), two-worker 4K render, ffmpeg encode, mux. **Ignore that skill's navy theme, palette and fonts.**
- **The VO wins over my note.** Map every beat to the actual word timestamps. If the words differ from my note, follow the VO and say so in one line.
- Output: 3840×2160, 29.97 fps (30000/1001), H.264 `-preset veryfast -crf 18 -pix_fmt yuv420p`, duration = exactly the VO. Send **only** `Name_4K_vo_sfx.mp4` (VO 0 dB + SFX −8 dB, `alimiter=limit=0.89`). Revisions: `_v2`, `_v3`.
- Before 4K, render 6–10 half-scale stills (`python3 render.py tst 0.5 t1 t2 …`), stack them in one contact sheet and look at it: centred, nothing clipped or touching the frame edge, nothing overlapping, readable on a phone. Then render 4K.
- Add font-hinting off to every cairo context that draws text (no jitter while the camera moves):
  `FO = cairo.FontOptions(); FO.set_hint_style(cairo.HINT_STYLE_NONE); FO.set_hint_metrics(cairo.HINT_METRICS_OFF); c.set_font_options(FO)`
- Render + encode script (`go.sh`, set DUR):
```bash
N=$(python3 -c "print(round(DUR*30000/1001))")
A=$(python3 -c "print(' '.join(str(i/(30000/1001)) for i in range(0,$N,2)))"); B=$(python3 -c "print(' '.join(str(i/(30000/1001)) for i in range(1,$N,2)))")
python3 render.py o 2 $A > r0.txt 2>&1 & python3 render.py o 2 $B > r1.txt 2>&1 & wait
ffmpeg -nostdin -v error -y -framerate 30000/1001 -i o/%04d.png -c:v libx264 -preset veryfast -crf 18 -pix_fmt yuv420p s.mp4
ffmpeg -v error -y -i s.mp4 -i seq.wav -i sfx.wav -filter_complex "[1:a]aresample=48000,volume=0dB[vo];[2:a]volume=-8dB[fx];[vo][fx]amix=inputs=2:normalize=0:duration=first,alimiter=limit=0.89[a]" -map 0:v -map "[a]" -c:v copy -c:a aac -b:a 256k -shortest NAME_4K_vo_sfx.mp4
```
- After sending: one line per beat (what appears on which word), then at most 2–3 lines on anything to check. No step recap.

## Reference script (render.py) — copy, then retime/re-asset
```python
#!/usr/bin/env python3
import math, os, sys
import numpy as np, cairo, cv2
OUT = sys.argv[1]; S = float(sys.argv[2]) if len(sys.argv) > 2 else 2.0
ONLY = [float(x) for x in sys.argv[3:]]; os.makedirs(OUT, exist_ok=True)
FPS = 30000 / 1001; DUR = 5.573
W, H = int(1920 * S), int(1080 * S)
HERE = os.path.dirname(os.path.abspath(__file__))

def clamp(x, a=0., b=1.): return max(a, min(b, x))
def lin(t, a, b): return clamp((t - a) / (b - a)) if b != a else float(t >= a)
def eio(x): x = clamp(x); return x * x * (3 - 2 * x)
def eout(x): x = clamp(x); return 1 - (1 - x) ** 3
def eq(x): x = clamp(x); return 1 - (1 - x) ** 5
def ec(x): x = clamp(x); return 4*x*x*x if x < .5 else 1 - (-2*x+2)**3/2
def eback(x, s=1.1):
    x = clamp(x); x -= 1; return x*x*((s+1)*x + s) + 1
def mix(a, b, k): return a + (b - a) * k

# ---------------- card images ----------------
SRC = {k: cv2.imread(os.path.join(HERE, 'cards', k + '.png'), cv2.IMREAD_UNCHANGED)
       for k in ['jw1','jw2','jw3','apple','i18','i17','i16','i15','i14','i13','i12','i11','ixs','ix']}
ASPECT = 1800 / 2400
_cache = {}
def surf_for(key, hpx):
    b = max(64, int(math.ceil(hpx / 48.0) * 48))
    ck = (key, b)
    if ck in _cache: return _cache[ck]
    im = SRC[key]; h = b; w = int(round(h * ASPECT))
    r = cv2.resize(im, (w, h), interpolation=cv2.INTER_AREA).astype(np.float32)
    a = r[..., 3:4] / 255.0
    pm = np.concatenate([r[..., :3] * a, r[..., 3:4]], 2).clip(0, 255).astype(np.uint8)
    pm = np.ascontiguousarray(pm)
    s = cairo.ImageSurface.create_for_data(memoryview(pm), cairo.FORMAT_ARGB32, w, h, w * 4)
    # shadow
    pad = int(h * 0.12)
    sa = np.zeros((h + 2*pad, w + 2*pad), np.float32); sa[pad:pad+h, pad:pad+w] = a[..., 0]
    sa = cv2.GaussianBlur(sa, (0, 0), h * 0.035)
    sh = np.zeros((h + 2*pad, w + 2*pad, 4), np.uint8); sh[..., 3] = (sa * 255).astype(np.uint8)
    sh = np.ascontiguousarray(sh)
    ss = cairo.ImageSurface.create_for_data(memoryview(sh), cairo.FORMAT_ARGB32, w + 2*pad, h + 2*pad, (w + 2*pad) * 4)
    _cache[ck] = (s, ss, w, h, pad, pm, sh)
    return _cache[ck]

def draw_card(c, key, cx, cy, hw, t_shine=None, alpha=1.0, sx=1.0, sy=1.0, dark=0.0, zoom=1.0):
    """card centred at world (cx,cy), height hw (world units). sx = horizontal flip squash."""
    if alpha <= 0.002 or abs(sx) < 0.004: return
    s, ss, w, h, pad, _, _ = surf_for(key, hw * S * zoom * max(sy, 1.0))
    k = hw / h
    c.save(); c.translate(cx, cy); c.scale(k * abs(sx), k * sy)
    # shadow
    c.save(); c.translate(-w/2 - pad, -h/2 - pad + h * 0.035)
    c.set_source_surface(ss, 0, 0); c.paint_with_alpha(0.75 * alpha); c.restore()
    c.translate(-w/2, -h/2)
    c.set_source_surface(s, 0, 0); c.get_source().set_filter(cairo.FILTER_GOOD)
    c.paint_with_alpha(alpha)
    if dark > 0:
        c.set_source_rgba(0, 0, 0, dark * alpha); c.mask_surface(s, 0, 0)
    if t_shine is not None and 0 < t_shine < 1:
        p = mix(-0.35, 1.35, eio(t_shine))
        L = math.hypot(w, h); ux, uy = w / L, h / L; bw = L * 0.16
        px_, py_ = p * w, p * h
        g = cairo.LinearGradient(px_ - ux*bw, py_ - uy*bw, px_ + ux*bw*0.8, py_ + uy*bw*0.8)
        for off, a in ((0, 0), (0.45, 0.10), (0.62, 0.42), (0.70, 0.20), (1.0, 0)):
            g.add_color_stop_rgba(off, 1, 1, 1, a * alpha)
        c.set_source(g); c.mask_surface(s, 0, 0)
    c.restore()

# ---------------- timeline ----------------
TICK = 17.0
def tick_gradient(y0, y1, a):
    g = cairo.LinearGradient(0, y0, 0, y1)
    g.add_color_stop_rgba(0, 1, 1, 1, a); g.add_color_stop_rgba(0.5, 0.86, 0.87, 0.89, a); g.add_color_stop_rgba(1, 0.62, 0.63, 0.66, a)
    return g

def draw_timeline(c, xs_major, x_start, x_end, y, t_head_glow, alpha, lead=5):
    """ticks from x_start to x_end (world), majors at xs_major (only those <= x_end+1)."""
    if alpha <= 0: return
    n_lead = lead
    xs = []
    x = x_start - n_lead * TICK
    while x <= x_end + 0.01:
        xs.append(x); x += TICK
    for x in xs:
        fade = 1.0
        if x < x_start - 0.01: fade = clamp(1 - (x_start - x) / (n_lead * TICK + 1)) ** 1.2
        major = any(abs(x - m) < TICK * 0.5 for m in xs_major)
        hh = 34 if major else 15
        # head pop: newest ticks grow in
        d = (x_end - x) / TICK
        grow = eout(clamp(d / 2.5 + 0.25)) if d < 2.5 else 1.0
        hh *= grow
        glow = clamp(1 - d / 6.0) * t_head_glow
        a = alpha * fade * (0.62 + 0.38 * glow if not major else 1.0)
        lw = 3.6 if major else 2.6
        c.set_source(tick_gradient(y, y + hh, a)); c.rectangle(x - lw/2, y + (34 - hh) / 2 if not major else y, lw, hh); c.fill()
        if glow > 0.02:
            c.set_source_rgba(1, 1, 1, 0.35 * glow * alpha); c.rectangle(x - lw, y - 2, lw * 2, hh + 4); c.fill()
    # thin baseline with sheen
    if x_end > x_start:
        g = cairo.LinearGradient(x_start - n_lead*TICK, 0, x_end, 0)
        g.add_color_stop_rgba(0, 0.8, 0.8, 0.82, 0); g.add_color_stop_rgba(0.08, 0.8, 0.8, 0.82, 0.45*alpha)
        g.add_color_stop_rgba(1, 1, 1, 1, 0.75*alpha)
        c.set_source(g); c.rectangle(x_start - n_lead*TICK, y + 34 + 6, x_end - x_start + n_lead*TICK, 1.6); c.fill()

def text_c(c, s, x, y, size, alpha, rise=0.0):
    if alpha <= 0: return
    c.save()
    c.select_font_face('Pricedown', 0, 0); c.set_font_size(size)
    e = c.text_extents(s)
    c.move_to(x - (e.x_advance) / 2, y + rise)
    c.text_path(s)
    g = cairo.LinearGradient(0, y - size * 0.75 + rise, 0, y + rise)
    g.add_color_stop_rgba(0, 1, 1, 1, alpha); g.add_color_stop_rgba(1, 0.86, 0.87, 0.89, alpha)
    c.set_source_rgba(0, 0, 0, 0.45 * alpha); c.save(); c.translate(0, 3); c.fill_preserve(); c.restore()
    c.set_source(g); c.fill()
    c.new_path(); c.restore()

# ---------------- layout ----------------
# John Wick row (world y=0)
JH = 500.0; JW_X = [0.0, 460.0, 920.0]; JW_Y = -40.0
JW_T = [0.98, 1.80, 2.36]          # "hit", "sequel", "2"
JW_YEARS = ['2014', '2017', '2019']
YEAR_Y = JW_Y + JH/2 + 72
TL_Y = JW_Y + JH/2 + 98

# iPhone row (world y=-1060)
IKEYS = ['i18','i17','i16','i15','i14','i13','i12','i11','ixs','ix']
IH0 = 540.0; R = 0.86; IY = -1060.0
IH = [IH0 * R**i for i in range(10)]
IWd = [h * ASPECT for h in IH]
tot = IWd[0] + sum(0.8 * w for w in IWd[1:])
left = 460 - tot / 2
IX = []
x = left
for i, w in enumerate(IWd):
    if i == 0: IX.append(x + w/2); x += w
    else: IX.append(x - 0.2*w + w/2); x = x - 0.2*w + w
T_TRAIL = [None] + [4.42 + (i-1) * 0.075 for i in range(1, 10)]
I_YEAR_Y = IY + IH0/2 + 72
I_TL_Y = IY + IH0/2 + 98

def camera(t):
    keys = [(0.0, 0, 28, 1.14), (1.78, 0, 28, 1.14), (2.30, 230, 28, 1.07), (2.32, 230, 28, 1.07), (2.90, 460, 28, 1.0),
            (3.28, 460, 28, 0.995), (4.12, -60, IY + 50, 1.0), (4.36, -60, IY + 50, 1.0), (5.52, 460, IY + 40, 0.86)]
    for (t0, x0, y0, z0), (t1, x1, y1, z1) in zip(keys, keys[1:]):
        if t <= t1:
            k = ec(lin(t, t0, t1))
            return mix(x0, x1, k), mix(y0, y1, k), math.exp(mix(math.log(z0), math.log(z1), k))
    return keys[-1][1:]

# ---------------- background ----------------
yy, xx = np.mgrid[0:H, 0:W].astype(np.float32)
nx, ny = xx / W, yy / H
d = np.sqrt(((nx - 0.30) * 1.25) ** 2 + ((ny - 0.05) * 0.95) ** 2)
lum = 11.5 + 15.5 * np.clip(1 - d / 1.05, 0, 1) ** 1.35
BG = np.repeat(lum[..., None], 3, 2)
BG[..., 0] += 0.6  # hint cool
VIG = (1 - 0.22 * (((xx - W/2)/(W/2))**2 + ((yy - H/2)/(H/2))**2) ** 1.5).clip(0.5, 1)[..., None]
GRAIN = cv2.resize(np.random.default_rng(3).random((H//3, W//3)).astype(np.float32), (W, H))[..., None]
del yy, xx, nx, ny, d, lum

def render(t):
    surf = cairo.ImageSurface(cairo.FORMAT_ARGB32, W, H); c = cairo.Context(surf)
    c.scale(S, S)
    cx, cy, z = camera(t)
    c.translate(960, 540); c.scale(z, z); c.translate(-cx, -cy)

    # ---- transition parameters ----
    flip1 = eio(lin(t, 3.38, 3.86))       # jw3 -> apple
    move = ec(lin(t, 3.34, 4.12))         # jw3 card travels to iPhone slot
    flip2 = eio(lin(t, 4.10, 4.46))       # apple -> iPhone 18
    jw_fade = 1 - eio(lin(t, 3.55, 4.05))

    # ---- John Wick row ----
    for i in range(3):
        t0 = JW_T[i]
        if t < t0: continue
        a_in = eq(lin(t, t0, t0 + 0.45))
        sc = mix(0.62, 1.0, eback(lin(t, t0, t0 + 0.62), 0.9))
        if i < 2:
            draw_card(c, 'jw%d' % (i+1), JW_X[i], JW_Y, JH * sc, t_shine=lin(t, t0 + 0.12, t0 + 0.92),
                      alpha=a_in * jw_fade, zoom=z)
        else:
            if flip1 <= 0:
                draw_card(c, 'jw3', JW_X[2], JW_Y, JH * sc, t_shine=lin(t, t0 + 0.12, t0 + 0.92), alpha=a_in, zoom=z)
        # year
        ya = eq(lin(t, t0 + 0.18, t0 + 0.6)) * jw_fade
        text_c(c, JW_YEARS[i], JW_X[i], YEAR_Y, 58, ya, rise=(1 - ya) * 14)

    # JW timeline
    if t >= JW_T[0]:
        g1 = eout(lin(t, 1.80, 2.30)); g2 = eout(lin(t, 2.36, 2.95))
        x_end = mix(JW_X[0], JW_X[1], g1) if g2 <= 0 else mix(JW_X[1], JW_X[2], g2)
        x_end += 4 * TICK * eout(lin(t, 2.4, 3.1))
        majors = [JW_X[0]] + ([JW_X[1]] if g1 > 0.98 else []) + ([JW_X[2]] if g2 > 0.98 else [])
        head = max(lin(t, 1.80, 2.32) * (1 - lin(t, 2.32, 2.6)), lin(t, 2.36, 2.96) * (1 - lin(t, 2.96, 3.3)))
        draw_timeline(c, majors, JW_X[0], x_end, TL_Y, head, eq(lin(t, JW_T[0] + 0.2, JW_T[0] + 0.6)) * jw_fade)

    # ---- iPhone row timeline + years (behind cards) ----
    if t > 4.30:
        k_last = 0
        for i in range(1, 10):
            if t >= T_TRAIL[i]: k_last = i
        prog = 0.0
        if t >= T_TRAIL[1]:
            prog = (t - T_TRAIL[1]) / (T_TRAIL[9] + 0.35 - T_TRAIL[1])
        x_end = mix(IX[0], IX[9], eout(prog))
        majors = [IX[0]] + ([IX[9]] if prog >= 0.99 else [])
        head = clamp(prog * 4) * (1 - lin(t, T_TRAIL[9] + 0.35, T_TRAIL[9] + 0.6))
        draw_timeline(c, majors, IX[0], x_end, I_TL_Y, head, eq(lin(t, 4.30, 4.6)), lead=4)
        a0 = eq(lin(t, 4.34, 4.7)); text_c(c, '2026', IX[0], I_YEAR_Y, 58, a0, rise=(1-a0)*14)
        a9 = eq(lin(t, T_TRAIL[9] + 0.18, T_TRAIL[9] + 0.5)); text_c(c, '2016', IX[9], I_YEAR_Y, 58, a9, rise=(1-a9)*14)

    # ---- trail cards (draw back to front) ----
    for i in range(9, 0, -1):
        t0 = T_TRAIL[i]
        if t < t0: continue
        k = eq(lin(t, t0, t0 + 0.42))
        x = mix(IX[i-1] + (IWd[i-1] - IWd[i]) * 0.0, IX[i], k)
        sc = mix(0.9, 1.0, k)
        draw_card(c, IKEYS[i], x, IY, IH[i] * sc, t_shine=None, alpha=eq(lin(t, t0, t0 + 0.25)),
                  dark=0.035 * i, zoom=z)

    # ---- the travelling flip card (jw3 -> apple -> iPhone 18) ----
    if flip1 > 0:
        px = mix(JW_X[2], IX[0], move); py = mix(JW_Y, IY, move)
        # small arc: lift slightly above the straight path
        py -= math.sin(math.pi * move) * 60
        hgt = mix(JH, JH, move)
        if flip2 > 0: hgt = mix(JH, IH0, eio(flip2))
        if flip2 <= 0:
            ang = flip1 * math.pi
            key = 'jw3' if ang < math.pi / 2 else 'apple'
            shine = None
        else:
            ang = flip2 * math.pi
            key = 'apple' if ang < math.pi / 2 else 'i18'
            shine = None
        sx = math.cos(ang); sy = 1 + 0.05 * math.sin(ang)
        dk = 0.45 * math.sin(ang)
        draw_card(c, key, px, py, hgt, t_shine=shine, alpha=1.0, sx=sx, sy=sy, dark=dk, zoom=z)

    surf.flush()
    arr = np.ndarray((H, W, 4), np.uint8, surf.get_data()).astype(np.float32)
    a = arr[..., 3:4] / 255.0
    img = BG * (1 - a) + arr[..., :3]
    return img

def post(img, t):
    img = img * (0.975 + 0.05 * GRAIN)
    small = cv2.GaussianBlur(cv2.resize(img, (W//8, H//8), interpolation=cv2.INTER_AREA), (0, 0), 5)
    img = img + cv2.resize(small, (W, H)) * 0.10
    return np.clip(img * VIG, 0, 255).astype(np.uint8)

N = int(round(DUR * FPS))
for fi in ([int(round(x * FPS)) for x in ONLY] if ONLY else range(N)):
    t = fi / FPS
    cv2.imwrite(os.path.join(OUT, f'{fi:04d}.png'), post(render(t), t), [cv2.IMWRITE_PNG_COMPRESSION, 1])
```

## Reference sound script (build_sfx.py)
```python
import sys; sys.path.insert(0,'/root/sfx')
from sfx import *
DUR=5.573; m=Mix(DUR)
m.add(0, drone(DUR, f=45), -26)
def shimmer(d=0.5):
    n=int(d*SR); x=RNG.standard_normal(n); t=np.arange(n)/SR
    y=bp(x,5000,12000)*np.sin(np.pi*np.linspace(0,1,n))**2
    return norm(y)
for t0 in (0.98,1.80,2.36):
    m.add(t0-0.05, whoosh(0.45,400,3000), -22, pan=0)
    m.add(t0+0.02, sub_hit(80,40,0.6), -24)
    m.add(t0+0.15, shimmer(0.6), -30, pan=0.3)
    m.add(t0+0.2, tick(2200,0.03), -30)
for k in range(14): m.add(1.80+k*0.035, tick(3200,0.015), -36)
for k in range(16): m.add(2.36+k*0.035, tick(3200,0.015), -36)
m.add(3.30, whoosh(0.85,200,2500), -19)
m.add(3.38, paper(0.3), -24); m.add(3.62, blip(700,1100,0.08), -30)
#m.add(3.86, shimmer(0.5), -30)
m.add(4.08, whoosh(0.4,600,5000), -23); m.add(4.30, sub_hit(90,38,0.9), -19)
#m.add(4.46, shimmer(0.7), -29)
m.add(4.36, whoosh(1.1,300,3000), -25)
for i in range(9): m.add(4.42+i*0.075, tick(1800+i*150,0.025), -29, pan=-0.3+i*0.07)
for k in range(30): m.add(4.42+k*0.03, tick(3400,0.012), -38)
m.add(5.15, confirm(), -27)
m.render('sfx.wav')
```
