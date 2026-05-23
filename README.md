
# Arduino Sonar Radar System

![Project Status](https://img.shields.io/badge/status-complete-brightgreen)
![Arduino](https://img.shields.io/badge/Arduino-Compatible-blue)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

## Overview

This project is a **low-cost, ultrasonic sonar radar system** built using an Arduino microcontroller. The system uses an HC-SR04 ultrasonic sensor mounted on a rotating servo motor to scan a 180-degree area, detect objects, and display their positions on a real-time graphical radar interface.

Unlike LIDAR-based systems, this design uses sonar (sound waves) and is significantly smaller, more affordable, and perfect for learning about embedded systems, serial communication, and data visualization.

## Features

- **180° Scanning Range** – Servo motor rotates the ultrasonic sensor to sweep the environment
- **Real-Time Distance Detection** – Calculates object distances using the speed of sound
- **Graphical Radar Display** – Processing software visualizes detected objects with a radar-style interface
- **Adjustable Range** – Configurable detection distance (default up to 400cm)
- **Serial Communication** – Real-time data transmission between Arduino and Processing
<img width="2125" height="1206" alt="IMG_0722 2" src="https://github.com/user-attachments/assets/6bafd7cc-54e4-48de-a876-f0e3787ce2f3" />
<img width="4283" height="5711" alt="IMG_0721" src="https://github.com/user-attachments/assets/d19b39d0-550e-4109-9f53-6ff24bb6ea09" />

## Components Required

| Component | Quantity | Notes |
|-----------|----------|-------|
| Arduino Uno (or compatible) | 1 | Any Arduino board with at least 2 digital pins |
| HC-SR04 Ultrasonic Sensor | 1 | For distance measurement using sound waves |
| SG-90 Micro Servo Motor | 1 | 180-degree rotation for sensor scanning |
| Breadboard | 1 | For prototyping connections |
| Jumper Wires (Male-to-Female) | 5-7 | For connecting components |
| 5V Power Supply (USB or external) | 1 | To power Arduino and servo |

*Optional: 3D-printed mount to attach the ultrasonic sensor to the servo motor.*

## Circuit Wiring Diagram

Connect the components to your Arduino as follows:

| HC-SR04 Sensor | Arduino Pin |
|----------------|-------------|
| VCC | 5V |
| GND | GND |
| Trig | Pin 9 |
| Echo | Pin 10 |

| Servo Motor | Arduino Pin |
|-------------|-------------|
| Red (VCC) | 5V |
| Brown/Black (GND) | GND |
| Orange/Yellow (Signal) | Pin 8 |

**Important:** The servo motor draws significant current. For stable operation, consider using an external 5V power supply for the servo. Connect the servo ground to the Arduino ground for a common reference.

## Software Requirements

| Software | Version | Purpose |
|----------|---------|---------|
| Arduino IDE | 1.8.19+ | Upload code to Arduino |
| Processing IDE | 4.0+ | Run radar visualization |
| HC-SR04 Library (optional) | NewPing | Simplified sensor control |

## Installation & Setup

### 1. Clone or Download the Project

```bash
git clone https://github.com/jaydenbrown3678![Uploading IMG_0721.jpeg…]()
/arduino-sonar-radar.git
cd arduino-sonar-radar
