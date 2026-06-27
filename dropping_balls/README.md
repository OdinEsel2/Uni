# BALLS

A zero-install, single-file video renderer that drops **2¹⁰ (1024) balls** inside a circle and lets them diverge into glowing, additive light-trails — a real-time visualization of chaos / sensitivity to initial conditions.

![dropping balls inside a circle](https://img.shields.io/badge/render-additive%20glow-8fb6ff)

## Run it

Open **`index.html`** in a browser (Chrome recommended for video recording). No build step, no dependencies.

## Controls

- **Number of balls** — text input (default 1024) with quick buttons for 2⁸–2¹⁶. Type any value.
- **Initial Drop · Noise**
  - *Position noise* — how far apart each ball starts (the "slight offset" that seeds the chaos).
  - *Velocity noise* — random spread on initial velocity.
  - *Drop height, launch speed, launch angle* — shape the initial throw.
- **Physics** — gravity, bounce (restitution), sim speed.
- **Look** — trail length, glow size, brightness, hue, saturation.

## Buttons & keys

| Action | Button | Key |
| --- | --- | --- |
| Re-drop | ↻ Re-drop | `Space` |
| Rewind to the original drop | ⏪ Rewind | `←` |
| Pause | ⏸ Pause | `P` |
| Record video (WebM/MP4) | ● Record | `R` |
| Save PNG still | ⤓ PNG | |
| Hide panel | ⤡ Hide | `H` |

**Rewind** replays the motion backwards all the way to frame 0. It uses deterministic replay — the original drop plus a tiny per-frame control log and bounded checkpoints — so it always reaches the start no matter how long the sim has run.

**Record** captures the canvas (controls are an HTML overlay, so they're not in the recording) and downloads a video file when you stop.
