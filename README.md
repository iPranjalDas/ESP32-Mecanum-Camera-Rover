# ESP32-Mecanum-Camera-Rover

[![Arduino](https://img.shields.io/badge/Arduino-Prototyping-00979D?style=for-the-badge&logo=arduino)](https://www.arduino.cc/)
[![Category](https://img.shields.io/badge/Category-Omni-Wheeled_Robotics-00e5ff?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](#)
[![Author](https://img.shields.io/badge/Author-Pranjal_Das-orange?style=for-the-badge)](https://github.com/iPranjalDas)

🏎️ Omnidirectional 4-wheel drive Mecanum rover with live ESP32-CAM video streaming & web teleoperation.

---

## 🖥️ System Architecture & Visual Wiring Layout

### 🔌 Graphical Schematic & Pinout Diagrams

![Camera Car with Mecanum Wheels](Diagrams/Camera%20Car%20with%20Mecanum%20Wheels.png)



```
┌── ESP32 MECANUM CAMERA ROVER SYSTEM ────────────────────────────────────┐
│                                                                         │
│   [ESP32-CAM Video Server]          [ESP32 Motion Controller]           │
│   OV2640 Lens ──> Web Stream        WiFi / WebSockets Telemetry         │
│   GPIO 4 Flashlight                 UART Link ──> ESP32-CAM             │
│                                                                         │
│          ┌──────────────────────────────────────────┐                   │
│          │         4x INDEPENDENT PWM CHANNELS      │                   │
│          └──────────────────────────────────────────┘                   │
│               │            │             │            │                 │
│               ▼            ▼             ▼            ▼                 │
│           [Front-L]    [Front-R]     [Rear-L]     [Rear-R]              │
│            Mecanum      Mecanum       Mecanum      Mecanum              │
│            45° Roll     45° Roll      45° Roll     45° Roll             │
│   DIAGONAL VECTORING: Strafe Left/Right | Pivot 360° | Diagonal Drift   │
└─────────────────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Hardware Requirements & Components

- **Microcontroller / Core:** Arduino Uno / ESP32 / NodeMCU (Refer to `.ino` sketch)
- **Power Supply:** 5V / 12V external regulated battery pack
- **Sensors & Actuators:** Detailed in circuit diagram and sketch pinout headers

---

## 🚀 Installation & Upload

1. Clone this repository:
   ```bash
   git clone https://github.com/iPranjalDas/ESP32-Mecanum-Camera-Rover.git
   ```
2. Open the primary `.ino` sketch in the [Arduino IDE](https://www.arduino.cc/en/software).
3. Install required libraries via the Arduino Library Manager.
4. If this sketch uses Wi-Fi, update `YOUR_WIFI_SSID` and `YOUR_WIFI_PASSWORD` with your local network settings.
5. Select your target board and COM port, then click **Upload**.

---

## 🔒 Security & Privacy Notice
All source sketches have been thoroughly sanitized. Generic placeholder strings are used for network credentials and API tokens.

---

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.  
Copyright (c) 2026 Pranjal Das. All Rights Reserved.

---

## 👤 Author & Architecture
**Pranjal Das**  
- **GitHub:** [@iPranjalDas](https://github.com/iPranjalDas)
- **Projects:** [https://iPranjalDas.github.io/Projects/](https://iPranjalDas.github.io/Projects/)
