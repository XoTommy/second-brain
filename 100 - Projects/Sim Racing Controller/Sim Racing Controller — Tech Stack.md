# ⚙️ Sim Racing Controller — Tech Stack

Parent: [[Sim Racing Controller]]

---

## Mobile App
- Framework: Flutter
- Platforms: Android first, iOS later
- Gyroscope input: Flutter sensors package
- WebSocket client: connects to PC companion app

---

## PC Companion App
- Language: Python
- Communication: WebSocket server
- Sim Rig preset: vJoy (DirectInput device)
- Other presets: ViGEm (XInput/Xbox device)
- Runs silently in background

---

## Connection Flow
1. PC companion app starts → opens WebSocket server
2. Phone app connects over WiFi to PC IP
3. Phone sends controller inputs as WebSocket messages
4. PC app receives inputs → feeds into vJoy or ViGEm
5. Game detects virtual controller → plays normally

---

## Key Libraries
- vJoy: virtual DirectInput joystick driver
- ViGEm: virtual Xbox/XInput controller driver
- Python websockets: WebSocket server
- Flutter sensors_plus: gyroscope access