#  Wearable Device to Detect Blood Blockage in Early Stages

A non-invasive IoT-based wearable health monitoring device built using 
ESP32 microcontroller and MAX30102 PPG sensor that monitors 5 blood 
health parameters in real time.

---

##  Project Overview

Blood vessel blockage is a leading cause of heart attack and stroke. 
Most people do not detect it until it becomes critical. This project 
provides an affordable, non-invasive wearable solution for continuous 
blood health monitoring at home without any hospital visit.

---

##  Parameters Monitored

| Parameter        | Description                          |
|------------------|--------------------------------------|
| BPM              | Heart Rate monitoring                |
| SpO₂             | Blood Oxygen Level                   |
| Hemoglobin       | Blood protein level (trend-based)    |
| Glucose          | Blood sugar trend estimation         |
| Blockage Status  | Normal / Slight / Medium / High      |

---

##  Hardware Components

| Component              | Specification                        |
|------------------------|--------------------------------------|
| ESP32 Microcontroller  | 240 MHz, WiFi 2.4GHz, 3.3V          |
| MAX30102 PPG Sensor    | IR 880nm, Red 660nm, 1.8V-3.3V      |
| OLED Display           | 0.96 inch, 128x64 pixels, I2C       |
| Jumper Wires           | 20cm, upto 5V                        |
| PCB Board              | General purpose perf board           |
| 9V Battery             | Portable power supply                |

---

##  How It Works

1. Finger is placed on MAX30102 sensor
2. Sensor emits Red light (660nm) and IR light (880nm) through finger
3. ESP32 processes the light absorption signals
4. All 5 parameters are calculated in real time
5. Results displayed on OLED screen
6. Data sent to IoT web dashboard via WiFi hotspot
7. Alert triggered when readings cross normal range

---

## 📊 IoT Dashboard Features

- Real-time graphs for BPM, Glucose and Hemoglobin
- Live parameter values displayed
- Last 10 readings stored as history table
- Automatic alert system for abnormal readings
- WiFi hotspot based — no internet required
- Accessible from any mobile or laptop browser

---

##  Software & Tools Used

- Arduino IDE — firmware development
- Embedded C — programming language
- HTML + JavaScript — IoT dashboard
- WiFi WebServer library — dashboard hosting
- Adafruit SSD1306 — OLED display library
- MAX30105 library — PPG sensor library

---

## 📁 Project Structure
wearable-blood-blockage-detection/
│
├── src/
│   └── main.ino          — Main ESP32 firmware code
│
├── dashboard/
│   └── index.html        — IoT web dashboard (embedded in code)
│
├── docs/
│   ├── circuit_diagram.png
│   └── project_report.pdf
│
├── images/
│   ├── prototype.jpg
│   └── dashboard_screenshot.png

