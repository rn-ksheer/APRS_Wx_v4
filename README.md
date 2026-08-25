# 📡 APRS_Wx_v4 — ESP32 Web-Configurable Weather Station

> ##### 🚧 WORK IN PROGRESS . . .
· · ·

Configure your **APRS weather beacon settings** entirely through your browser — **no hardcoding, no sketch modifications, and absolutely no dependency nightmares**. 😈

<img src="https://github.com/user-attachments/assets/66c5de3c-2fb3-4ce3-96a6-1faa1181bcd0" alt="APRS_Wx_v4 Prototype" width="28%">

---

## ✨ Features

- 🔧 **Fully browser-configurable** — APRS callsign, GPS coordinates, beacon interval, Wi-Fi settings, and more.
- 💾 **Persistent storage** — Settings are saved to flash and survive reboots.
- 🔁 **Live configuration** — Make changes without reflashing the firmware.
- 📱 **Mobile-friendly interface** — Configure your station from a phone, tablet, or laptop.
- 📡 **AP + STA mode** — Easy initial setup and reliable day-to-day operation.
- 🔒 **OTA firmware updates** *(planned)* — Upload new firmware directly from your browser.

---

## 📦 Hardware Requirements

- ✅ **ESP32-based microcontroller**
- ✅ A supported **weather sensor**, depending on the selected firmware
- ✅ **5V USB power supply** or a suitable **5–6V adapter**
- ✅ **Optional OLED display**

---

## 🔌 Wiring Connections

> **Note:** Wiring depends on the sensor and firmware you are using. Please refer to the project documentation/PDF for complete build instructions.

### ESP32 to DHT11 / DHT22

| ESP32 | Sensor |
|:-----:|:------:|
| 🔴 **3.3V** | **VCC** |
| ⚫ **GND** | **GND** |
| 🟢 **GPIO 4 (D4)** | **Signal / DATA** |

### ESP32 to BMP180 / BMP280 / BME280 (I²C)

| ESP32 | Sensor |
|:-----:|:------:|
| 🔴 **3.3V** | **VCC / VIN** |
| ⚫ **GND** | **GND** |
| 🟢 **GPIO 21 (SDA)** | **SDA** |
| 🔵 **GPIO 22 (SCL)** | **SCL** |

---

## 🔁 Resetting Configuration

To change or reset your station settings:

1. Put the device into **Configuration Mode**.
2. Open the configuration page in your browser.
3. Make the required changes and save them.

The new settings will be stored in flash memory and retained after a reboot.

---

## 🔧 Dependencies

The firmware uses several libraries and utilities, including:

- ESPAsyncWebServer
- EEPROM
- WiFiManager
- APRS packet formatting utilities
- And many more...

> 😊 These dependencies are **pre-integrated into the firmware**, so you do **not** need to worry about manually managing library versions.

---

## 📖 Build & Prototype Instructions

> **All instructions required to build and test the prototype are provided in the project PDF/documentation.**

### 🖥️ ESP32 Flash Download Tool

[![Download ESP32 Flasher](https://img.shields.io/badge/Download-ESP32%20Flasher-blue?style=for-the-badge&logo=github)](https://github.com/rn-ksheer/APRS_Wx_v4/raw/main/flash_download_tool_3.9.5.zip)

---

## 🌡️ Supported Sensors & Hardware

| Supported Hardware |
|:------------------|
| DHT11 |
| DHT22 |
| BMP180 |
| BMP280 |
| BME280 |
| OLED Display |

### 📝 Sensor Capabilities

> - ➡️ **BMP180** — Temperature, pressure, and altitude
> - ➡️ **BMP280** — Temperature, pressure, and altitude
> - ➡️ **BME280** — Temperature, pressure, altitude, and humidity
> - ➡️ Both **BMP280** and **BME280** modules are available in **4-pin and 6-pin versions**. They can look very similar and may be difficult to distinguish visually.
> - ➡️ To avoid compatibility issues, always purchase sensors from a **reliable and reputable seller**.

---

## 📊 BMP180 vs BMP280

| Feature | BMP180 *(Older Generation)* | BMP280 *(Next Generation)* |
|:---|:---|:---|
| **Pressure Range** | 300 to 1100 hPa | 300 to 1100 hPa |
| **Relative Accuracy** | ±0.12 hPa (approx. ±1 metre) | ±0.12 hPa (approx. ±1 metre) |
| **Absolute Accuracy** | ±1.0 hPa | ±1.0 hPa |
| **RMS Noise** | 0.06 hPa (Advanced mode) | 0.0016 hPa (Ultra High Resolution) |
| **Interfaces Supported** | I²C only | I²C and SPI |
| **Current Consumption** | 5 µA (at 1 sample/sec.) | 2.7 µA (at 1 sample/sec.) |
| **Footprint Size** | 3.6 mm × 3.8 mm | 2.0 mm × 2.5 mm |

---

## 📥 Firmware Downloads

![Download Firmware](https://img.shields.io/badge/Download-Firmware-blue?style=for-the-badge&logo=github)

| Sensor / Configuration | Firmware Version | Download |
|:---|:---:|:---:|
| **DHT11** | 4.1.0 | [⬇️ Download](https://github.com/rn-ksheer/APRS_Wx_v4/raw/main/DHT11/v3.4.5.bin) |
| DHT11 + OLED 1.3" | — | Coming soon |
| DHT11 + OLED 0.96" | — | Coming soon |
| DHT22 | — | Coming soon |
| DHT22 + OLED 1.3" | — | Coming soon |
| DHT22 + OLED 0.96" | — | Coming soon |
| BMP180 | — | Coming soon |
| BMP180 + OLED 1.3" | — | Coming soon |
| BMP180 + OLED 0.96" | — | Coming soon |
| **BMP280** | — | [⬇️ Download](https://github.com/rn-ksheer/APRS_Wx_v4/raw/main/BMP280/v3.4.4.bin) |
| BMP280 + OLED 1.3" | — | Coming soon |
| BMP280 + OLED 0.96" | — | Coming soon |
| **BME280** | 4.1.0 | [⬇️ Download](https://github.com/rn-ksheer/APRS_Wx_v4/raw/main/BME280/v3.4.5.bin) |
| BME280 + OLED 1.3" | — | Coming soon |
| BME280 + OLED 0.96" | — | Coming soon |

> 💡 **Tip:** Download the firmware that matches your exact sensor and hardware configuration.

---

## 📡 Tracking Your Weather Station

Once your **callsign and APRS passcode are correctly configured**, your weather station will automatically start appearing on [**aprs.fi**](https://aprs.fi/) after it successfully transmits and is received by the APRS network.

You can use **aprs.fi** to view your station's location, weather telemetry, packets, and other APRS activity.

---

## 🛠️ Roadmap

- [ ] Display sensor data on the OLED screen
- [ ] Password protection for the configuration web page
- [ ] OTA firmware upload via the web interface
- [ ] Support for digipeater functionality
- [ ] Display live sensor data on the web page
- [ ] Advanced beacon scheduling

---

### 📌 Project Status

This project is actively under development. More sensor combinations, display support, and additional APRS features will be added over time.

**73! 📡**

 > ##### My Iteration Versions:
 > - Nodemcu - v1
 > - esp8266-01 - v2
 > - Wemos D1 Mini - v3
 > - ESP32 - v4


<!--[![Download Firmware](https://img.shields.io/badge/Download-Firmware-blue?style=for-the-badge&logo=github)](https://github.com/rn-ksheer/APRS_Wx_v4/raw/main/BME280/v3.4.5.bin)-->

