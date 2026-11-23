# Prompt: "Rockstar Money Run" animation (logo + growing icon grid + hero card)

Paste this into a new chat, then attach the VO clip and (if you have them) the logo PNG, the hero card image and an optional intro video.

You are my motion designer. Recreate my **"Rockstar Money Run"** animation for the new VO I attach, exactly in this style, retimed to the new words. A reference script is at the end: copy it, change only the beat times, assets and counts, and keep everything else (layout, easing, colours, background) as it is.

## What the animation is
1. **Optional intro clip** (only if I attach a video): it plays at 90% scale inside a rounded rectangle (radius 38, 6 px white border, soft shadow) on the charcoal background, with a slow push-in. On the word where the topic turns to the company, the camera glides **down** the canvas (cubic in-out, ~0.65 s). The clip slides **up and fully out of frame** before the logo settles, never a hard cut. I can name an offset ("start the video from 5 s"); extract the frames from that point. If there is no clip, start directly on the logo.
2. **Logo pop** on the company's name (default: Rockstar logo PNG, upscaled ×3 with Lanczos + light unsharp): scale 0.15 → 1 with back-ease overshoot (s=2.0, 0.62 s), a small −9° rotation that settles straight, a soft drop shadow, then a **soft glare** sweeping top-left → bottom-right (starts 0.3 s after the pop, 0.65 s long). No white flash.
3. **Shift left** on the next key phrase: the logo moves from centre (height 430) to x=318 (height 300) over 0.62 s while the camera pulls back from 1.10 to 1.0.
4. **Icon grid** builds as a left→right column sweep (each column ~0.03 s after the previous, small random jitter per icon, each icon rises 14 px and scales 0.6 → 1 over 0.22 s), filling the space between the logo and the card.
   - **Dollars** (default): 8 rows × 33 columns of Pricedown `$`, size 40, pitch 28 × 44, purple (top `#C785FF` → bottom `#8F47DB`).
   - The last few per row are **missing in a non-uniform pattern**, e.g. `[3, 1, 5, 2, 6, 2, 4, 1]`. Make it look deliberate, not uniform.
   - On the "not there / missing / ready" word I name, the missing ones appear at ~20% opacity and **blink** (2.6 blinks/s, sharpened cosine, 6%↔22%) until the end.
5. **Hero card** pops on the right (x=1618, 300×400) on the word I name (default: GTA VI). It has 3:4 chamfered corners (11% of width), a dark gradient `rgb(.13,.10,.16)` → `rgb(.05,.04,.07)` and a soft pink/purple radial glow. The real logo is at 80% width, at its optical centre (GTA VI: −5.4% x, +4% y). Border: 3.2 px white → light grey. Shadow: **one smooth blurred shadow** (Gaussian), never stacked layers. Pop: scale 0.2 → 1, back-ease s=1.9, 0.6 s.
6. Final framing: logo left, grid middle, card right, all on one horizontal line, centred, with a slow drift to zoom 0.985.

## People variant ("only N out of 100 …")
Same logo + card. The grid is 100 solid pictogram people (round head r=7.2, rounded torso, two legs; light grey `rgb(.80,.82,.86)`) in 5 rows × 20 columns, pitch 45 × 70, built with the same sweep.
- On "N" (the number), N scattered people turn GTA purple and blink (3.2 Hz, 30%↔100% with a faint purple glow).
- On the next word ("players"/"people"), they lift out one by one (0.06 s stagger, slight upward arc, scale 1.55) and line up just **above the first row**, leaving faint 14% ghosts.
- "N OUT OF 100" pops in under the grid in Pricedown 58 (white, black stroke 6%, soft shadow), and the rest dim to 38%.
- **Follow-up clip** ("those N were enough"): start on the exact last frame. On the phrase, purple square brackets with a black stroke open from the centre around the N (0.45 s), and the N blink again. On "enough", the bracket + people pop up 10% and settle. **Never green for these.**

## Assets
- Rockstar logo PNG: ask me if not attached.
- GTA VI logo: download `https://raw.githubusercontent.com/homarr-labs/dashboard-icons/main/svg/grand-theft-auto-vi.svg`, render with cairosvg at 1600 px, crop to the alpha bbox.
- GTA Online / GTA V topics use the GTA V card I send. Never use a plain "Grand Theft Auto" wordmark when GTA 6 is meant.

## Files the reference script expects (next to render.py)
`rockstar_up.png` (logo, upscaled), `gta6.png` (hero logo, alpha-cropped), `clip/%04d.jpg` (intro frames at 3456×1944, `ffmpeg -ss OFFSET -t 3.3 -i clip.mp4 -vf "fps=30000/1001,scale=3456:1944:flags=lanczos"`). With no intro clip, delete `draw_clip` and start the camera on the logo section.

## Sound (`build_sfx.py`)
- Drone bed −27 dB.
- Camera-down whoosh −19 dB.
- Logo pop: `sub_hit(110,40)` −17 + `blip` −24, then a quiet shimmer under the glare.
- Shift: whoosh −24.
- Grid: one `tick` per column −31 (+ a blip every 3rd column −36).
- Card: whoosh −24 + `sub_hit` −19 + blip −25.
- One soft low `blip(420)` per missing-blink, fading out.

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
FPS = 30000 / 1001; DUR = 6.433
W, H = int(1920 * S), int(1080 * S)
HERE = os.path.dirname(os.path.abspath(__file__))

def clamp(x, a=0., b=1.): return max(a, min(b, x))
def lin(t, a, b): return clamp((t - a) / (b - a)) if b != a else float(t >= a)
def eio(x): x = clamp(x); return x * x * (3 - 2 * x)
def eout(x): x = clamp(x); return 1 - (1 - x) ** 3
def eq(x): x = clamp(x); return 1 - (1 - x) ** 5
def ec(x): x = clamp(x); return 4*x*x*x if x < .5 else 1 - (-2*x+2)**3/2
def eback(x, s=1.7):
    x = clamp(x) - 1; return x*x*((s+1)*x + s) + 1
def mix(a, b, k): return a + (b - a) * k

def to_surface(bgra):
    """bgra uint8 straight alpha -> premultiplied cairo surface (keeps buffer alive)"""
    f = bgra.astype(np.float32); a = f[..., 3:4] / 255.0
    pm = np.ascontiguousarray(np.concatenate([f[..., :3] * a, f[..., 3:4]], 2).clip(0, 255).astype(np.uint8))
    h, w = pm.shape[:2]
    s = cairo.ImageSurface.create_for_data(memoryview(pm), cairo.FORMAT_ARGB32, w, h, w * 4)
    return s, pm

def shadow_surface(alpha, blur):
    h, w = alpha.shape; pad = int(blur * 3)
    sa = np.zeros((h + 2*pad, w + 2*pad), np.float32); sa[pad:pad+h, pad:pad+w] = alpha
    sa = cv2.GaussianBlur(sa, (0, 0), blur)
    sh = np.zeros(sa.shape + (4,), np.uint8); sh[..., 3] = (sa * 255).astype(np.uint8)
    s, buf = to_surface(sh)
    return s, buf, pad

# ---------------- assets ----------------
RS = cv2.imread(os.path.join(HERE, 'rockstar_up.png'), cv2.IMREAD_UNCHANGED)
RS_SURF, RS_BUF = to_surface(RS)
RS_SH, RS_SHB, RS_PAD = shadow_surface(RS[..., 3] / 255.0, RS.shape[0] * 0.035)
RS_W, RS_H = RS.shape[1], RS.shape[0]

G6 = cv2.imread(os.path.join(HERE, 'gta6.png'), cv2.IMREAD_UNCHANGED)
_ys, _xs = np.where(G6[..., 3] > 8); G6 = np.ascontiguousarray(G6[_ys.min():_ys.max()+1, _xs.min():_xs.max()+1])
G6_SURF, G6_BUF = to_surface(G6)
G6_W, G6_H = G6.shape[1], G6.shape[0]

# ---------------- layout (world, design px) ----------------
CLIP_W, CLIP_H = 1728.0, 972.0; CLIP_X, CLIP_Y = 960.0, 540.0; CLIP_R = 38.0
SY = 1380.0                      # Rockstar section centre y
RS_X0, RS_S0 = 960.0, 430.0      # logo centred, height
RS_X1, RS_S1 = 318.0, 300.0      # logo after shift
CARD_X, CARD_W, CARD_H = 1618.0, 300.0, 400.0
ROWS, COLS = 8, 33
PITCH_X, PITCH_Y = 28.0, 44.0
GX0 = 528.0                      # first column centre
GY0 = SY - (ROWS - 1) * PITCH_Y / 2
MISS = [3, 1, 5, 2, 6, 2, 4, 1]  # missing dollars at the end of each row
RNG = np.random.default_rng(7)
JIT = RNG.uniform(0, 0.07, (ROWS, COLS))
PURPLE_T = (0.78, 0.52, 1.00); PURPLE_B = (0.56, 0.28, 0.86)

T_POP = 2.68; T_SHIFT = 3.06; T_BUILD0, T_BUILD1 = 3.30, 3.98; T_CARD = 4.24; T_READY = 4.30

def camera(t):
    keys = [(0.0, 960, 540, 1.0), (2.36, 960, 540, 1.035), (3.02, 960, SY, 1.10), (3.06, 960, SY, 1.10),
            (3.70, 960, SY, 1.0), (DUR, 960, SY, 0.985)]
    for (t0, x0, y0, z0), (t1, x1, y1, z1) in zip(keys, keys[1:]):
        if t <= t1:
            k = ec(lin(t, t0, t1))
            return mix(x0, x1, k), mix(y0, y1, k), math.exp(mix(math.log(z0), math.log(z1), k))
    return keys[-1][1:]

def rrect(c, x, y, w, h, r):
    c.new_sub_path(); c.arc(x+w-r, y+r, r, -math.pi/2, 0); c.arc(x+w-r, y+h-r, r, 0, math.pi/2)
    c.arc(x+r, y+h-r, r, math.pi/2, math.pi); c.arc(x+r, y+r, r, math.pi, 1.5*math.pi); c.close_path()

def chamfer(c, x, y, w, h, k):
    c.move_to(x + k, y); c.line_to(x + w - k, y); c.line_to(x + w, y + k); c.line_to(x + w, y + h - k)
    c.line_to(x + w - k, y + h); c.line_to(x + k, y + h); c.line_to(x, y + h - k); c.line_to(x, y + k); c.close_path()

_clip_cache = {}
def clip_frame(t):
    i = min(98, int(round(t * FPS))) + 1
    if i not in _clip_cache:
        _clip_cache.clear()
        im = cv2.imread(os.path.join(HERE, 'clip', f'{i:04d}.jpg'))
        if S != 2.0: im = cv2.resize(im, (int(CLIP_W * S), int(CLIP_H * S)), interpolation=cv2.INTER_AREA)
        bgra = np.dstack([im, np.full(im.shape[:2], 255, np.uint8)])
        bgra = np.ascontiguousarray(bgra)
        s = cairo.ImageSurface.create_for_data(memoryview(bgra), cairo.FORMAT_ARGB32, bgra.shape[1], bgra.shape[0], bgra.shape[1] * 4)
        _clip_cache[i] = (s, bgra)
    return _clip_cache[i][0]

def draw_clip(c, t):
    x, y = CLIP_X - CLIP_W / 2, CLIP_Y - CLIP_H / 2 - 520 * ec(lin(t, 2.36, 2.98))
    # shadow
    for k, a in ((26, 0.10), (14, 0.14), (6, 0.18)):
        c.set_source_rgba(0, 0, 0, a); rrect(c, x - k * 0.5, y + k * 0.6, CLIP_W + k, CLIP_H + k, CLIP_R + k * 0.5); c.fill()
    s = clip_frame(t)
    c.save(); rrect(c, x, y, CLIP_W, CLIP_H, CLIP_R); c.clip()
    c.translate(x, y); c.scale(CLIP_W / s.get_width(), CLIP_H / s.get_height())
    c.set_source_surface(s, 0, 0); c.get_source().set_filter(cairo.FILTER_GOOD); c.paint(); c.restore()
    c.set_line_width(6); c.set_source_rgba(1, 1, 1, 0.96); rrect(c, x, y, CLIP_W, CLIP_H, CLIP_R); c.stroke()

def glare(c, w, h, p, mask_surf, strength=1.0):
    L = math.hypot(w, h); ux, uy = w / L, h / L; bw = L * 0.17
    px_, py_ = p * w, p * h
    g = cairo.LinearGradient(px_ - ux*bw, py_ - uy*bw, px_ + ux*bw*0.8, py_ + uy*bw*0.8)
    for off, a in ((0, 0), (0.45, 0.12), (0.62, 0.62), (0.70, 0.26), (1.0, 0)):
        g.add_color_stop_rgba(off, 1, 1, 1, a * strength)
    c.set_source(g); c.mask_surface(mask_surf, 0, 0)

def draw_rockstar(c, t):
    if t < T_POP: return
    kp = lin(t, T_POP, T_POP + 0.62)
    sc = mix(0.15, 1.0, eback(kp, 2.0))
    a = eq(lin(t, T_POP, T_POP + 0.16))
    rot = (1 - eq(kp)) * math.radians(-9)
    ks = ec(lin(t, T_SHIFT, T_SHIFT + 0.62))
    x = mix(RS_X0, RS_X1, ks); hgt = mix(RS_S0, RS_S1, ks) * sc
    k = hgt / RS_H
    c.save(); c.translate(x, SY); c.rotate(rot); c.scale(k, k)
    c.save(); c.translate(-RS_W/2 - RS_PAD, -RS_H/2 - RS_PAD + RS_H * 0.04)
    c.set_source_surface(RS_SH, 0, 0); c.paint_with_alpha(0.8 * a); c.restore()
    c.translate(-RS_W/2, -RS_H/2)
    c.set_source_surface(RS_SURF, 0, 0); c.get_source().set_filter(cairo.FILTER_GOOD); c.paint_with_alpha(a)
    tg = lin(t, T_POP + 0.30, T_POP + 0.95)
    if 0 < tg < 1: glare(c, RS_W, RS_H, mix(-0.35, 1.35, eio(tg)), RS_SURF, 1.0)
    c.restore()

def dollar(c, x, y, size, alpha, lift=0.0):
    if alpha <= 0.003: return
    c.select_font_face('Pricedown', 0, 0); c.set_font_size(size)
    e = c.text_extents('$')
    c.move_to(x - e.x_advance / 2, y + size * 0.36 + lift)
    c.text_path('$')
    g = cairo.LinearGradient(0, y - size * 0.5 + lift, 0, y + size * 0.5 + lift)
    g.add_color_stop_rgba(0, *PURPLE_T, alpha); g.add_color_stop_rgba(1, *PURPLE_B, alpha)
    c.set_source(g); c.fill(); c.new_path()

def draw_grid(c, t):
    if t < T_BUILD0 - 0.05: return
    span = T_BUILD1 - T_BUILD0
    blink = 0.0
    if t >= T_READY:
        k = t - T_READY
        sq = 0.5 + 0.5 * math.cos(2 * math.pi * 2.6 * k)          # 2.6 blinks / s
        sq = clamp((sq - 0.5) * 3 + 0.5)                           # sharpened -> blink
        blink = eq(lin(t, T_READY, T_READY + 0.12)) * (0.06 + 0.16 * sq)
    for r in range(ROWS):
        n_have = COLS - MISS[r]
        y = GY0 + r * PITCH_Y
        for j in range(COLS):
            x = GX0 + j * PITCH_X
            if j < n_have:
                t0 = T_BUILD0 + span * (j / (COLS - 1)) + JIT[r, j] + r * 0.012
                k = eq(lin(t, t0, t0 + 0.22))
                if k <= 0: continue
                dollar(c, x, y, 40 * mix(0.6, 1.0, k), k, lift=(1 - k) * 14)
            elif blink > 0:
                dollar(c, x, y, 40, blink)

def draw_card(c, t):
    if t < T_CARD: return
    kp = lin(t, T_CARD, T_CARD + 0.6)
    sc = mix(0.2, 1.0, eback(kp, 1.9)); a = eq(lin(t, T_CARD, T_CARD + 0.15))
    c.save(); c.translate(CARD_X, SY); c.scale(sc, sc)
    w, h = CARD_W, CARD_H; x, y = -w/2, -h/2; ch = w * 0.11
    # ONE smooth blurred shadow (build once: chamfer mask -> GaussianBlur(22*S) -> ARGB surface), never stacked layers
    if CARD_SH is not None:
        srf, sw, shh, pad = CARD_SH; kk = w / (sw / S)
        c.save(); c.translate(0, 22 * kk); c.scale(kk / S, kk / S); c.translate(-(sw / 2 + pad), -(shh / 2 + pad))
        c.set_source_surface(srf, 0, 0); c.paint_with_alpha(0.75 * a); c.restore()
    g = cairo.LinearGradient(x, y, x + w, y + h)
    g.add_color_stop_rgba(0, 0.13, 0.10, 0.16, a); g.add_color_stop_rgba(1, 0.05, 0.04, 0.07, a)
    chamfer(c, x, y, w, h, ch); c.set_source(g); c.fill_preserve()
    c.save(); c.clip()
    rg = cairo.RadialGradient(0, 0, 10, 0, 0, w * 0.75)
    rg.add_color_stop_rgba(0, 0.85, 0.30, 0.65, 0.30 * a); rg.add_color_stop_rgba(1, 0.4, 0.1, 0.5, 0)
    c.set_source(rg); c.paint()
    lw_ = w * 0.80; k = lw_ / G6_W
    ox, oy = -0.054 * lw_, 0.040 * G6_H * k      # optical centre (logo weight sits right/top)
    c.save(); c.translate(-lw_/2 + ox, -G6_H * k / 2 + oy); c.scale(k, k)
    c.set_source_surface(G6_SURF, 0, 0); c.get_source().set_filter(cairo.FILTER_GOOD); c.paint_with_alpha(a); c.restore()
    c.restore()
    chamfer(c, x, y, w, h, ch); c.set_line_width(3.2)
    bg = cairo.LinearGradient(x, y, x + w, y + h)
    bg.add_color_stop_rgba(0, 1, 1, 1, 0.95 * a); bg.add_color_stop_rgba(1, 0.70, 0.70, 0.74, 0.9 * a)
    c.set_source(bg); c.stroke()
    c.restore()

def make_card_shadow():
    w, h = int(CARD_W * S), int(CARD_H * S); pad = int(80 * S)
    m = cairo.ImageSurface(cairo.FORMAT_A8, w + 2 * pad, h + 2 * pad); mc = cairo.Context(m)
    chamfer(mc, pad, pad, w, h, w * 0.11); mc.set_source_rgba(0, 0, 0, 1); mc.fill(); m.flush()
    a = np.ndarray((m.get_height(), m.get_stride()), np.uint8, m.get_data())[:, :w + 2 * pad].astype(np.float32) / 255
    a = cv2.GaussianBlur(a, (0, 0), 22 * S)
    img = np.zeros(a.shape + (4,), np.uint8); img[..., 3] = (a * 255).astype(np.uint8)
    srf, buf = to_surface(img); globals()['_CSB'] = buf
    return (srf, w, h, pad)
CARD_SH = make_card_shadow()

# ---------------- background (same as previous animation) ----------------
yy, xx = np.mgrid[0:H, 0:W].astype(np.float32)
nx, ny = xx / W, yy / H
d = np.sqrt(((nx - 0.30) * 1.25) ** 2 + ((ny - 0.05) * 0.95) ** 2)
lum = 11.5 + 15.5 * np.clip(1 - d / 1.05, 0, 1) ** 1.35
BG = np.repeat(lum[..., None], 3, 2); BG[..., 0] += 0.6
VIG = (1 - 0.22 * (((xx - W/2)/(W/2))**2 + ((yy - H/2)/(H/2))**2) ** 1.5).clip(0.5, 1)[..., None]
GRAIN = cv2.resize(np.random.default_rng(3).random((H//3, W//3)).astype(np.float32), (W, H))[..., None]
del yy, xx, nx, ny, d, lum

def render(t):
    surf = cairo.ImageSurface(cairo.FORMAT_ARGB32, W, H); c = cairo.Context(surf)
    c.scale(S, S)
    cx, cy, z = camera(t)
    c.translate(960, 540); c.scale(z, z); c.translate(-cx, -cy)
    if t < 3.0: draw_clip(c, t)
    draw_grid(c, t)
    draw_card(c, t)
    draw_rockstar(c, t)
    surf.flush()
    arr = np.ndarray((H, W, 4), np.uint8, surf.get_data()).astype(np.float32)
    a = arr[..., 3:4] / 255.0
    return BG * (1 - a) + arr[..., :3]

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
DUR=6.433; m=Mix(DUR)
m.add(0, drone(DUR, f=45), -27)
def shimmer(d=0.5):
    n=int(d*SR); x=RNG.standard_normal(n)
    return norm(bp(x,5000,12000)*np.sin(np.pi*np.linspace(0,1,n))**2)
m.add(2.30, whoosh(0.8,250,2600), -19)
m.add(2.68, sub_hit(110,40,0.8), -17); m.add(2.70, blip(500,1300,0.09), -24)
m.add(2.98, shimmer(0.65), -27, pan=0.2)
m.add(3.02, whoosh(0.55,500,3500), -24, pan=-0.4)
for j in range(33):
    t=3.30+0.9*j/32
    m.add(t, tick(2400+RNG.uniform(-300,500),0.02), -31, pan=-0.6+1.2*j/32)
    if j%3==0: m.add(t+0.01, blip(1700,2100,0.03), -36, pan=-0.6+1.2*j/32)
m.add(4.20, whoosh(0.4,600,4500), -24, pan=0.6)
m.add(4.24, sub_hit(100,42,0.7), -19, pan=0.5); m.add(4.26, blip(800,1500,0.08), -25, pan=0.5)
for k in range(5):
    m.add(4.30+k/2.6, blip(420,420,0.12), -25 - k)
m.render('sfx.wav')
```
