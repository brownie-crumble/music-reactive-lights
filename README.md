# Music Reactive Lights

> Real-time audio-reactive LED system — music goes in, light show comes out.

Built with an **Arduino Nano** and a **WS2812B NeoPixel strip**, this system captures live audio through a microphone module, processes the signal on-board, and maps sound amplitude to dynamic color and brightness changes across the LED strip.

---

## 📹 Demo

https://github.com/brownie-crumble/music-reactive-lights/blob/master/Beats_normal.mp4

---

## How It Works
1. **Sound Detection** — Microphone module captures audio and converts it to an analog signal
2. **Signal Processing** — Arduino reads amplitude on A0 and maps it to LED parameters
3. **LED Control** — NeoPixel strip responds with real-time color and brightness changes

---

## Circuit Diagram

![Circuit Diagram](https://github.com/brownie-crumble/music-reactive-lights/raw/master/circuit%20diagram.png)

---

## Components

| Component | Details |
|---|---|
| Microcontroller | Arduino Nano |
| LED Strip | WS2812B NeoPixel (or similar) |
| Sound Sensor | Microphone module (analog out) |
| Resistor | 470Ω — data line protection |
| Capacitor | 1000µF — power stabilization |

---

## Wiring

**Sound Sensor → Arduino Nano**

| Sensor Pin | Arduino Pin |
|---|---|
| VCC | 5V |
| GND | GND |
| OUT | A0 |

**NeoPixel Strip → Arduino Nano**

| Strip Pin | Connection |
|---|---|
| DIN | D6 (via 470Ω resistor) |
| +5V | External 5V supply |
| GND | Common GND |

> ⚠️ Place a 1000µF capacitor across +5V and GND near the strip to prevent power surges on startup.

---

## Setup

1. Clone this repo
2. Open `code1.ino` in Arduino IDE
3. Install **Adafruit NeoPixel** library via Library Manager
4. Upload to Arduino Nano
5. Wire up per the diagram and power on

---

## Troubleshooting

| Symptom | Fix |
|---|---|
| LEDs not responding | Check power supply voltage and data line resistor |
| Inconsistent colors | Verify capacitor placement and GND connections |
| Sensor not detecting sound | Reposition mic module closer to audio source |
| Flickering LEDs | Ensure power supply can handle peak LED current draw |

---

## Tech Stack

`Arduino` `C++` `NeoPixel` `Embedded Systems` `IoT` `Signal Processing`
