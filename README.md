# APRS_Wx_v4
ESP32 based APRS Wx Station


## Firmware Download

👉 [Download the latest BME280 firmware](https://github.com/rn-ksheer/APRS_Wx_v4/BME280/v3.4.5.bin)


[![Download Firmware](https://img.shields.io/badge/Download-Firmware-blue?style=for-the-badge&logo=github)](https://github.com/rn-ksheer/APRS_Wx_v4/raw/main/BME280/v3.4.5.bin)



##### WORK IN PROGRESS . . .

# 📡  APRS_Wx_v4 ( ESP32 version) Web-Configurable

Configure your ***APRS beacon settings*** entirely through your browser — no hardcoding, no sketch modifications, and absolutely no dependency nightmares. :trollface:

<img src="https://github.com/user-attachments/assets/66c5de3c-2fb3-4ce3-96a6-1faa1181bcd0" alt="prototype" width=28% style="float:left"></p>


---

##### (Wx station As "minimalsitic" As Possible)

<img src="https://github.com/user-attachments/assets/a59915d9-7893-41ea-8c82-5707780325c4" alt="prototype" width="400" height="300" style="float:left"></p>

---

## ✨ Features
- 🔧 **Fully browser-configurable**: APRS callsign, GPS Coordinates, interval, WiFi, and more.
- 💾 **Persistent storage**: Settings are saved to flash and survive reboots.
- 🔁 **Live configuration**: Changes take effect without reflashing firmware.
- 📱 **Mobile-friendly interface**: Configure from your phone, tablet, or laptop.
- 🔒 **Secure WiFi setup**: AP + STA mode for easy setup and permanent operation.
- 🌍 **OTA update support** *(optional)*: Upload new firmware from the browser. (future implementation) 
---

## 📦 Hardware Requirements
- ✅ **ESP32** –based microcontroller
- ✅ Sensors based on your selected `firmware`
- ✅ Power source (USB 5V or 5-6v adaptor)
- ✅ Optional: OLED display
---

## 🔌 Wiring Connections 🌐 Usage Guide
- Depends on your sensor / Check PDF.

## ESP32 to DHT11/DHT22 Wiring

| ESP32 | Sensor |
|:-----:|:-----:|
| 🔴**3.3V** | **VCC** |
| ⚫**GND** | **GND** |
| 🟢**GPIO 4 (D4)** | **Signal / DATA** |

## ESP32 to BMP180/BMP280/BME280 Wiring (I²C)

| ESP32 | Sensor |
|:-----:|:-----:|
| 🔴**3.3V** | **VCC / VIN** |
| ⚫**GND** | **GND** |
| 🟢**GPIO 21 (SDA)** | **SDA** |
| 🔵**GPIO 22 (SCL)** | **SCL** |


## 🔁 Resetting Configuration
To reset all settings:
- Put device in **Config mode** & make the required changes.
---

## 🔧 Dependencies
- ESPAsyncWebServer
- EEPROM
- WiFiManager
- APRS packet formatting utilities
- Many more . . .

These are **pre-integrated** in the firmware. You do **not** need to manage library versions manually . :smiley:

---



> ## All Instructions to build and test the prototype has been given in the pdf.
 

[![ESP32-flasher download](https://img.shields.io/badge/Download-Flasher-blue?style=for-the-badge&logo=github)](https://github.com/rn-ksheer/APRS_Wx_v4/raw/main/flash_download_tool_3.9.5.zip)




| Supported Sensors |
| :---: | 
| DHT11 | 
| DHT22 |
| BMP180  |
| BMP280  |
| BME280  |
| OLED Display  |


>**Note:** <br>
&#10687; ➡️BMP180 - Temperature Pressure altitude <br>
&#10687; ➡️BMP280 - Temperature Pressure altitude <br>
&#10687; ➡️BME280 - Temperature Pressure altitude humidity <br>
&#10687; Both BMP280 and BME280 modules are available in 4-pin and 6-pin versions. They often look identical and cannot be visually distinguished. <br>
&#10687; To avoid compatibility issues or errors, always purchase from a reliable and reputable seller.



| Feature | BMP180 (Older Generation) | BMP280 (Next Generation) |
| :--- | :--- | :--- |
| **Pressure Range** | 300 to 1100 hPa | 300 to 1100 hPa |
| **Relative Accuracy** | ±0.12 hPa (approx. ±1 metre) | ±0.12 hPa (approx. ±1 metre) |
| **Absolute Accuracy** | ±1.0 hPa | ±1.0 hPa |
| **RMS Noise** | 0.06 hPa (Advanced mode) | 0.0016 hPa (Ultra high res) |
| **Interfaces Supported** | I2C only | I2C and SPI |
| **Current Consumption** | 5 µA (at 1 sample/sec.) | 2.7 µA (at 1 sample/sec.) |
| **Footprint Size** | 3.6 mm x 3.8 mm | 2.0 mm x 2.5 mm |



| possible combinations | firmware version | Download |
| :---:  |     :---:        | :---:              |
| DHT11   | 4.1.0 | |	
| DHT11/OLED 1.3"  | | |	
| DHT11/OLED 0.96"  | | |	
| DHT22  |		
| DHT22/OLED 1.3"  | | |	
| DHT22/OLED 0.96"  | | |	
| BMP180  | 		
| BMP180/OLED 1.3"  | | |	
| BMP180/OLED 0.96"  | | |	
| BMP280  | 		
| BMP280/OLED 1.3"  | | |	
| BMP280/OLED 0.96"  | | |	
| BME280  | 		
| BME280/OLED 1.3"  | | |	
| BME280/OLED 0.96"  | | |	


## 🛠️ Roadmap
- [ ]  Display Sensor data on OLED screen
- [ ] Password protection for the config web page
- [ ] OTA firmware upload via web interface
- [ ] Support for digipeater functionality
- [ ] Display Sensor data on the web page
- [ ] Advanced beacon scheduling (time-of-day, speed-based, etc.)
---



 > ##### My Iteration Versions:
 > - Nodemcu - v1
 > - esp8266-01 - v2
 > - Wemos D1 Mini - v3
 > - ESP32 - v4
