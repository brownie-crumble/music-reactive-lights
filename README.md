# 🎵 Music Reactive Lights

An Arduino Nano + NeoPixel LED system that reacts to music in real-time — sound is captured via a microphone sensor, processed on-board, and mapped to dynamic color and brightness changes across the LED strip.

> Built with: Arduino Nano · WS2812B NeoPixel Strip · Sound Sensor (Microphone Module)

---

## Demo

<!-- Once you have a video/GIF, upload it to the repo and replace this line: -->
<!-- ![Demo GIF](demo.gif) -->
> 📹 Demo video coming soon

---

## How It Works

1. **Sound Detection** — Microphone module captures audio and outputs an analog signal
2. **Signal Processing** — Arduino Nano reads the signal on A0, maps amplitude to LED parameters
3. **LED Control** — NeoPixel strip responds with color and brightness changes in real-time

---

## Circuit Diagram

![Circuit Diagram](https://github.com/brownie-crumble/music-reactive-lights/raw/master/circuit%20diagram.png)

---

## Components

| Component | Spec |
|---|---|
| Microcontroller | Arduino Nano |
| LED Strip | WS2812B NeoPixel (or similar) |
| Sound Sensor | Microphone module (analog out) |
| Resistor | 470Ω (data line protection) |
| Capacitor | 1000µF (power stabilization) |

---

## Wiring

**Sound Sensor → Arduino**
- VCC → 5V
- GND → GND
- OUT → A0

**NeoPixel Strip → Arduino**
- DIN → D6 (via 470Ω resistor)
- +5V → External 5V supply (with 1000µF cap across +5V and GND)
- GND → Common GND

---

## Setup

1. Clone this repo
2. Open `code1.ino` in Arduino IDE
3. Install the `Adafruit NeoPixel` library (Library Manager)
4. Upload to Arduino Nano
5. Wire up per the diagram above and power on

---

## Troubleshooting

| Issue | Fix |
|---|---|
| LEDs not responding | Check power supply and data line resistor |
| Inconsistent colors | Verify capacitor placement and GND connections |
| Sensor not detecting | Reposition mic module closer to audio source |
