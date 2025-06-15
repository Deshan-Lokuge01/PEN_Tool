<h1 align="center">📡 Offensive & Defensive Wi-Fi/Bluetooth PEN Tool 🔐</h1>

<p align="center">


  <img src="https://img.shields.io/badge/Bluetooth-Supported-green" />
  <img src="https://img.shields.io/badge/WiFi-Hacking-orange" />
  <img src="https://img.shields.io/badge/Status-Prototype-lightgrey" />
</p>

---

## 🧠 Project Overview

This tool is a **compact, low-cost**, and **portable Wi-Fi/Bluetooth penetration testing device** developed using an **ESP32 microcontroller** with a **2.8" ILI9341 TFT touchscreen**.

It offers both **offensive and defensive capabilities** for ethical hackers and cybersecurity enthusiasts to audit wireless environments effectively.

---

## 🎯 Objectives

- ✅ Identify Wi-Fi/Bluetooth vulnerabilities
- ✅ Enhance signal strength & reduce noise
- ✅ Perform real-time and offline wireless security testing
- ✅ Use an intuitive TFT-based touchscreen UI with stylus
- ✅ Enable data logging via SD card for offline analysis

---

## ⚙️ Hardware Specifications

<div align="center">

<table>
  <tr>
    <th>Module</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>🎮 Microcontroller</td>
    <td>ESP32</td>
  </tr>
  <tr>
    <td>📺 Display</td>
    <td>2.8” ILI9341 TFT touchscreen</td>
  </tr>
  <tr>
    <td>💾 Storage</td>
    <td>SD Card module (for saving PCAPs and logs)</td>
  </tr>
  <tr>
    <td>🔋 Power Supply</td>
    <td>Battery / USB powered (5V input)</td>
  </tr>
  <tr>
    <td>📡 Antennas</td>
    <td>Optional external Wi-Fi/Bluetooth antenna</td>
  </tr>
</table>

</div>

---


## 🛠️ Features & Capabilities

### 🔧 Offensive Capabilities
- Beacon Spam (List, Random)
- Fake SSID Generation
- Probe Request Sniffing
- Wi-fi/Bluetooth Jamming
- Evil Portal Attacks (planned)
- Rick Roll Beacon Broadcasting

### 🛡️ Defensive Capabilities
- Detect Deauth Attacks (Detect kick-offed Devices )
- Detect Bluetooth Skimmers
- Monitor Packet Density (bar graph)

### 🔍 Wireless Recon
- Wi-Fi SSID/Channel/RSSI/Encryption scan
- Bluetooth Classic & BLE scan
- Packet sniffing (Wi-Fi & Bluetooth)
- PCAP logging to SD card

### 🎨 UI / UX
- Touchscreen GUI for mode selection
- Stylus input support
- Real-time status and scanning result views

---

## 🖼️ System Block Diagram

<div align="center">

🧩 **Functional Blocks**: ESP32 MCU, TFT Display, SD Card, Power Supply

<img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/EasyEDA_Sketch.jpg" alt="System Diagram" width="600"/>

</div>

---

## 🔋 Power Setup

- Supports both **battery-powered** and **USB operation**
- Designed for **field-ready deployment**

---

## 📦 Pin Configuration (ESP32 ↔ Modules)

<div align="center">

<table>
  <tr>
    <td>

<b>🔌 ILI9341 TFT Display</b>

<table>
  <tr><th>TFT Pin</th><th>ESP32 Pin</th></tr>
  <tr><td>VCC</td><td>3.3V</td></tr>
  <tr><td>GND</td><td>GND</td></tr>
  <tr><td>CS</td><td>D17</td></tr>
  <tr><td>RESET</td><td>D5</td></tr>
  <tr><td>DC</td><td>D16</td></tr>
  <tr><td>SDI (MOSI)</td><td>D23</td></tr>
  <tr><td>SCK</td><td>D18</td></tr>
  <tr><td>LED</td><td>D32</td></tr>
  <tr><td>SDO (MISO)</td><td>D19</td></tr>
  <tr><td><b>T_CLK</b></td><td>D18</td></tr>
  <tr><td><b>T_CS</b></td><td>D21</td></tr>
  <tr><td><b>T_DIN</b></td><td>D23</td></tr>
  <tr><td><b>T_DO</b></td><td>D13</td></tr>
  <tr><td><b>T_IRQ</b></td><td>Not Connected</td></tr>
</table>

</td>

<td style="width: 50px;"></td> <!-- spacing between tables -->

<td>

<b>💾 SD Card Module</b>

<table>
  <tr><th>SD Card Pin</th><th>ESP32 Pin</th></tr>
  <tr><td>CS</td><td>D12</td></tr>
  <tr><td>MOSI</td><td>D23</td></tr>
  <tr><td>MISO</td><td>D19</td></tr>
  <tr><td>SCK</td><td>D18</td></tr>
</table>

</td>
  </tr>
</table>

</div>

---
## 🧩 Fritzing Sketch

<div align="center">

<img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/Fritzing%20sketch.png" alt="Demonstration Activity" width="600"/>

<p><i>Illustration of ESP32 connected to a TFT display and SD card module using color-coded jumper wires.</i></p>

</div>

---

## 🧪 Real-Time Features

- Wi-Fi Analysis (SSID, channel)
- Bluetooth Scanning (names, addresses, RSSI)
- Fake AP Broadcasting
- Touch-based menu navigation
- Onboard keyboard for SSID input

---

## 🧊 Offline Analysis

- Store PCAP files on SD card
- Analyze with tools like **Wireshark**
- Export logs for documentation/reporting

---
## 🧩 Offensive & Defensive Activity Demonstration

<div align="center">

<img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/Demonstartion.png" alt="Demonstration Activity" width="1000"/>

</div>

### 📝 Description of the Above Demonstration

1️⃣ **Offensive Mode**  
The first screenshot demonstrates a **Deauthentication Attack** being sent to the target access point: **Dialog 4G 842**. The attack parameters were configured through the PEN Tool's touchscreen interface.

2️⃣ **Defensive Monitoring**  
The second screenshot shows **real-time monitoring** of the targeted AP's **MAC address and RSSI** using the PEN Tool. This operation is performed ethically within an authorized testing area.

3️⃣ **Validation of Attack**  
The third image confirms that devices connected to the targeted AP were successfully identified using the ARP table on a terminal. During the deauth attack, these connected clients were **disconnected (kicked off)** as expected.

---

## 📌 Constraints

- ❌ No cloud connectivity (offline-only by design)
- 📶 Range dependent on antenna quality
- ⛔ Randomized MAC address generating on devices

---

## 🔄 Enhancements

- Portable casing with 3D-printed enclosure
- Bluetooth evil portal implementation
- More advanced TFT GUI with animations
- Automatic PCAP parsing for quick summaries

---

## 🧑‍💻 Designed and Developed By:

📍 Department of Electrical and Information Engineering  
📚 Faculty of Engineering, University of Ruhuna  
📅 April 2025 | Module: EE6304 - Embedded Systems Design

---

## 📎 References

- [ESP32 Documentation](https://cdn.sparkfun.com/datasheets/IoT/esp32_datasheet_en.pdf)
- [Wireshark - Network Analyzer](https://www.wireshark.org/)
- [ILI9341 TFT Display Tutorial](https://academy.cba.mit.edu/classes/output_devices/TFT/ILI9341.pdf)
- [EasyEDA Circuit Design Tool](https://easyeda.com/)
- [Fritzing Breadboard Designer](https://fritzing.org/)

---

<p align="center">
  <strong>🔐 Secure the air. Audit the spectrum. Go ethical.</strong><br/>
  <code>#IoT #CyberSecurity #PenTesting #ESP32</code>
</p>

<div align="center">
  <h3 style="color:orange;">🚧 Note: This project is still in development 🚧</h3>
  <p><i>Further implementations, improvements, and feature enhancements may be added as development progresses.</i></p>
</div>


<div align="center">
  <h2 style="color: red;">⚠️ Use Only the Authorized Places ⚠️</h2>
</div>

