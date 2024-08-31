# Music Reactive Lights using Arduino Nano and NeoPixel LED Strip

This project creates a vibrant music-reactive light system using an Arduino Nano, a sound sensor, and a NeoPixel LED strip. The LEDs react dynamically to sound, changing colors and brightness based on the audio input, providing a visual representation of the music.

## Table of Contents
- [Introduction](#introduction)
- [Components Required](#components-required)
- [Circuit Diagram](#circuit-diagram)
- [How It Works](#how-it-works)
- [Setup Instructions](#setup-instructions)
- [Troubleshooting](#troubleshooting)

## Introduction

This project is designed to bring your music to life with lights. By using a sound sensor to capture audio signals, the system controls a strip of NeoPixel LEDs to create a light show that responds in real-time to the music's rhythm and intensity.

## Components Required

- Arduino Nano
- NeoPixel LED Strip (WS2812B or similar)
- Sound Sensor (Microphone module)
- 470Ω resistor (for data line)
- 1000µF capacitor (for power stabilization)
- Breadboard and jumper wires
- Power supply for the LED strip

## Circuit Diagram

Below is the block diagram for the project setup:

![Circuit Diagram](https://github.com/brownie-crumble/music-reactive-lights/raw/main/circuitdiagram.png)  

## How It Works

1. Sound Detection:
   - The sound sensor captures audio signals and converts them into an electrical signal.
   
2. Signal Processing:
   - The Arduino Nano processes the signal and determines the intensity and rhythm of the audio.

3. LED Control:
   - The Arduino controls the NeoPixel LED strip, adjusting the colors and brightness based on the processed audio signal.

## Setup Instructions

1. Connect the Sound Sensor:
   - VCC to 5V on Arduino
   - GND to GND on Arduino
   - OUT to A0 on Arduino

2. Connect the NeoPixel LED Strip:
   - DIN to Pin D6 on Arduino (through a 470Ω resistor)
   - +5V to 5V power supply (with a 1000µF capacitor across +5V and GND)
   - GND to common ground with Arduino

3. Power the System:
   - Connect the power supply to the LED strip and ensure all connections are secure.

## Troubleshooting

- LEDs Not Responding:
  - Check the connections and ensure the power supply is sufficient.

- Inconsistent Colors:
  - Verify the resistor and capacitor values are correct and connections are stable.

- Sound Sensor Not Detecting:
  - Make sure the sensor is properly connected and positioned to capture sound effectively.

