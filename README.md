# 💧 IoT-Based Water Level Monitoring System

## 📘 Project Overview

This project implements a smart **IoT-Based Water Level Monitoring System** using an **ESP32** microcontroller and an **HC-SR04 ultrasonic sensor**. It is designed to:

- Monitor water levels in a tank
- Display levels on an LCD
- Provide visual (LEDs) and audio (buzzer) alerts
- Transmit data to **ThingSpeak** for cloud-based remote monitoring


## 🛠️ Components Used

| Component        | Purpose                                |
|------------------|----------------------------------------|
| ESP32            | Main controller with Wi-Fi             |
| HC-SR04          | Measures water level                   |
| 16x2 LCD (I2C)   | Displays real-time water level         |
| Green LED        | Lights up when tank is full            |
| Yellow LED       | Lights up when water is at safe level  |
| Red LED          | Lights up when water is low            |
| Buzzer           | Sounds alert when overflow occurs      |

---

## 🔌 Connections

| Component          | ESP32 Pin        | Notes                             |
|--------------------|------------------|-----------------------------------|
| HC-SR04            | TRIG → GPIO5     | Signal pin                        |
|                    | ECHO → GPIO18    | Signal pin                        |
|                    | VCC → 3.3V       | Power                             |
|                    | GND → GND        | Ground                            |
| LCD (I2C)          | SDA → GPIO21     | I2C Communication                 |
|                    | SCL → GPIO22     | I2C Communication                 |
| Green LED          | GPIO15           | Via 330Ω resistor to GND          |
| Yellow LED         | GPIO2            | Via 330Ω resistor to GND          |
| Red LED            | GPIO4            | Via 330Ω resistor to GND          |
| Buzzer             | GPIO23           | Positive end                      |
| Wi-Fi (built-in)   | —                | Sends data to ThingSpeak          |

---

## 💻 Functional Highlights

- **Ultrasonic sensor** measures distance from tank top to water.
- **LEDs** indicate the water level:
  - Green → Full
  - Yellow → Normal
  - Red → Low
- **Buzzer** activates during overflow.
- **LCD display** shows real-time water status.
- **Wi-Fi enabled ESP32** uploads data to **ThingSpeak** every 2 seconds.

---
