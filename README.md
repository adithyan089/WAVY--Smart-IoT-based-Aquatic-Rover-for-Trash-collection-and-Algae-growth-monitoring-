# 🌊 WAVY – Smart Aquatic Trash Collection Rover
**An IoT-powered solution for waterbody waste cleanup, real-time monitoring, and algae-growth optimization**

![WAVY Banner](images/wavy_banner.jpg)

---

## 🚀 Project Overview

**WAVY** is an innovative smart aquatic rover designed for collecting floating waste from water surfaces while monitoring environmental conditions. Built using **ESP32**, **IR sensors**, **Ultrasonic**, and **DHT22**, it adapts its power usage based on the possibility of algae growth. With manual and autonomous control modes, WAVY ensures efficient and sustainable waterbody maintenance.

---

## 🎯 Key Features

- 🤖 Autonomous trash collection using IR sensors and obstacle avoidance
- 🌡️ Real-time temperature and humidity monitoring with DHT22
- ⚡ Algae-aware adaptive power optimization
- 📶 Web-based dashboard for manual control and monitoring
- 🔁 Manual/Auto mode switching with fallback logic
- 🔋 Low-power operation based on environmental conditions
- 🛠️ Motor driver (L298N) + Relay-controlled conveyor mechanism

---

## 📷 System Images

| Working Prototype | Web UI Interface | On-Water Testing |
|-------------------|------------------|------------------|
| ![rover](images/rover_front_view.jpg) | ![ui](images/web_dashboard.jpg) | ![test](images/rover_water_test.jpg) |

---

## 📡 System Architecture

![WAVY System Architecture](images/wavy_architecture_diagram.png)

---

## 🔧 Hardware Components

- ESP32 Dev Board
- IR Sensors (2x) – Left & Right edge detection
- Ultrasonic Sensor – Obstacle detection
- DHT22 – Atmospheric temperature and humidity
- L298N Motor Driver – Dual paddle wheel control
- 100 RPM Conveyor Motor – Trash collection
- Relay Module (2-channel) – Motor control
- Li-ion Battery (7.4V) + Buck Converter
- Plastic body with grip-conveyor and floating base

---

## 💻 Software & Libraries

- **Arduino IDE / PlatformIO**
- WebServer Library for ESP32
- DHT Sensor Library
- HTML + JavaScript for Web Dashboard
- Firebase/Local UI (optional for logs)

---

## ⚙️ Setup Instructions

### 1. Wiring Connections

- **IN1–IN4, ENA, ENB** → Motor Driver
- **GPIO 34, 35** → IR Sensors
- **GPIO 4** → DHT22
- **GPIO 5 (Trig), GPIO 18 (Echo)** → Ultrasonic Sensor
- **GPIO 12** → Relay for conveyor
- Power: 7.4V → Buck Converter → 5V output to ESP32 and sensors

### 2. Upload Firmware

```bash
# In Arduino IDE:
- Select Board: ESP32 Dev Module
- Install necessary libraries (WebServer, DHT, etc.)
- Upload `main.ino` from `code/` folder
