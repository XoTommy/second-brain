# 🎮 Sim Racing Controller — Features & Presets

Parent: [[Sim Racing Controller]]

---

## Preset 1 — Standard Xbox Layout
- Full Xbox controller button layout on screen
- Connects as XInput device via ViGEm
- Detected as Xbox controller by all games

---

## Preset 2 — Racing Preset
- Xbox layout base
- Gyroscope tilt steering added
- Tilt phone left/right to steer
- Connects via ViGEm

---

## Preset 3 — Sim Rig (Hero Feature)
- Touchable steering wheel graphic on screen
- Auto-returns to neutral when finger lifts
- Two sliding pressure pedals — throttle + brake
- Sliding upward increases pedal pressure
- Connects as DirectInput device via vJoy
- Games detect it as a real sim racing wheel
- Compatible: Forza Horizon 5, Assetto Corsa, BeamNG

---

## PC Companion App
- Lightweight Python app
- Runs in system background
- Receives inputs over WebSocket
- Feeds inputs into vJoy (Sim Rig) or ViGEm (other presets)
- No UI needed — just runs silently

---

## V1 Limitations
- No force feedback in V1
- No layout customization in free tier
- No sensitivity customization in free tier