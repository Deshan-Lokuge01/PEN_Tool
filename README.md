<h1 align="center">📡 Offensive & Defensive Wi-Fi/Bluetooth PEN Tool 🔐</h1>

<p align="center">

  <img src="https://img.shields.io/badge/ESP 32-Based-yellow" />
  <img src="https://img.shields.io/badge/WiFi-Hacking-orange" />
  <img src="https://img.shields.io/badge/Bluetooth-Supported-green" />
  <img src="https://img.shields.io/badge/Device-Poratable-magenta" />
</p>

---

<div align="center">

🧩 **Esp32 Based PEN Tool**

<table>
  <tr>
    <td><img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/logo.jpg" alt="WiFi Sniffers" width="250"/></td>
    <td><img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/01.jpg" alt="WiFi Options" width="250"/></td>
    <td><img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/05.jpg" alt="WiFi Sniffers" width="250"/></td>
    <td><img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/02.2.jpg" alt="WiFi Attacks" width="250"/></td>
    
  </tr>
</table>

</div>

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
<table>
<tr valign="top">
<td width="25%">
<h4><u>🔧 Offensive Capabilities</u></h4>
<ul>
<li>Beacon Spam (List, Random)</li>
<li>Fake SSID Generation</li>
<li>Probe Request Sniffing</li>
<li>Wi-fi/Bluetooth Jamming</li>
<li>Evil Portal Attacks (planned)</li>
<li>Rick Roll Beacon Broadcasting</li>
</ul>
</td>
<td width="25%">
<h4><u>🛡️ Defensive Capabilities</u></h4>
<ul>
<li>Detect Deauth Attacks</li>
<li>Detect Bluetooth Skimmers</li>
<li>Monitor Packet Density</li>
</ul>
</td>
<td width="25%">
<h4><u>🔍 Wireless Recon</u></h4>
<ul>
<li>Wi-Fi SSID/Channel/RSSI Scan</li>
<li>Bluetooth Classic & BLE Scan</li>
<li>Packet Sniffing</li>
<li>PCAP Logging to SD card</li>
</ul>
</td>
<td width="25%">
<h4><u>🎨 UI / UX</u></h4>
<ul>
<li>Touchscreen GUI</li>
<li>Stylus Input Support</li>
<li>Real-time Status Views</li>
</ul>
</td>
</tr>
</table>

---

## 🔬 In-Depth Feature Breakdown

### 📶 Wi-Fi Operations

<div align="center">

🧩 **Wifi Options (Sniffing / Attacks / General)**

<img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/02.1.png" alt="System Diagram" width="600"/>

</div>


🔍 Wi-fi Sniffing (Silently Listening)

<table>
  <thead>
    <tr>
      <th width="30%">Feature</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><span style="color:blue">Probe Request Sniffer</span></td>
      <td>Checks for probe requests when a device is searching for nearby SSIDs. It lists the MAC addresses of nearby devices, like phones, helping to determine which devices are in an area.</td>
    </tr>
    <tr>
      <td><span style="color:blue">Beacon Sniffer</span></td>
      <td>Sniffs out and lists nearby Wi-Fi Access Points (APs) only.</td>
    </tr>
    <tr>
      <td><b>Scan and Save APs List</b></td>
      <td>Scans for and saves a list of nearby APs for later analysis.</td>
    </tr>
    <tr>
      <td><b>De-auth Sniffer</b></td>
      <td>Searches for deauthentication packets, allowing you to observe if another device is being kicked off a network during an attack.</td>
    </tr>
    <tr>
      <td><b>EAPOL/PMKID Scan</b></td>
      <td>Captures specific authentication packets (EAPOL/PMKID) used in WPA/WPA2 handshakes. These can be saved to an SD card and used with tools like Hashcat for offline password cracking.</td>
    </tr>
    <tr>
      <td><b>Raw Capture</b></td>
      <td>Captures and displays the MAC addresses of all nearby devices along with their RSSI (signal strength).</td>
    </tr>
    <tr>
      <td><b>Station Sniffer</b></td>
      <td>After selecting a target AP, this feature sniffs out and lists all client devices that are connected to that specific network. This is useful for planning a targeted deauth attack.</td>
    </tr>
    <tr>
      <td><b>Signal Monitor</b></td>
      <td>Shows the real-time signal strength for the network you are currently connected to.</td>
    </tr>
  </tbody>
</table>

⚠️ Wi-Fi Attacks

<table>
<thead>
<tr>
<th width="30%">Attack Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><b>Beacon Spam List</b></td>
<td>Floods the network with fake Wi-Fi networks (SSIDs) using a pre-saved list of names.</td>
</tr>
<tr>
<td><b>Beacon Spam Random</b></td>
<td>Generates and broadcasts a large number of random, fake Access Points to clutter the network, which can be very disruptive.</td>
</tr>
<tr>
<td><b>Rick Roll Beacon</b></td>
<td>Broadcasts Wi-Fi network names (SSIDs) that are lines from the lyrics of Rick Astley's classic song.</td>
</tr>
<tr>
<td><b>Probe Request Flood</b></td>
<td>Floods a target Access Point with rapid probe requests, which can jam the AP and prevent legitimate devices from connecting.</td>
</tr>
<tr>
<td><b>De-auth Flood</b></td>
<td>Broadcasts deauthentication packets to all nearby Access Points, disconnecting all clients within range.</td>
</tr>
<tr>
<td><b>AP Clone Spam</b></td>
<td>Broadcasts cloned SSIDs of legitimate access points from a saved list to confuse users and facilitate other attacks.</td>
</tr>
<tr>
<td><b>Deauth Targeted</b></td>
<td>Allows you to select a specific device (client) connected to a network and send targeted deauthentication packets to disconnect only that single device.</td>
</tr>
</tbody>
</table>

⚙️ Wi-fi General

- Normal Functionalities are there. (Add Generate, Clear SSIDs, Select APs, Stations)
Typically, Encryptions. Then we can save them into the SD card.


### 🔵 Bluetooth Operations

<div align="center">

🧩 **Wifi Options (Sniffing / Attacks / General)**

<img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/Picture1.png" alt="System Diagram" width="600"/>

</div>

<table>
<thead>
<tr>
<th width="30%">Feature / Attack</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" align="center"><b>Bluetooth Attacks</b></td>
</tr>
<tr>
<td><b>Sour Apple</b></td>
<td>Spoofs Bluetooth Low Energy (BLE) advertisements that mimic Apple devices, potentially causing pop-ups on iPhones and iPads.</td>
</tr>
<tr>
<td><b>Swiftpair Spam</b></td>
<td>Targets Windows 10/11 systems by sending BLE ads that mimic devices ready to pair, causing repeated "Tap to connect" pop-ups.</td>
</tr>
<tr>
<td><b>Samsung BLE Spam</b></td>
<td>Targets Samsung devices by spoofing BLE peripherals they try to auto-recognize, which can trigger connection dialogs.</td>
</tr>
<tr>
<td><b>BLE Spam All</b></td>
<td>A combination mode that runs all BLE spam attacks simultaneously to simulate a Denial of Service (DoS) or stress-test scenario on all nearby BLE devices.</td>
</tr>
<tr>
<td colspan="2" align="center"><b>Bluetooth Sniffers</b></td>
</tr>
<tr>
<td><b>Bluetooth Sniffer</b></td>
<td>Scans for and lists nearby Bluetooth devices.</td>
</tr>
<tr>
<td><b>Detect Card Skimmers</b></td>
<td>Specifically looks for known Bluetooth signatures of common credit card skimmers used in ATMs or point-of-sale machines.</td>
</tr>
</tbody>
</table>
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

## 🧩 Evil Portal Attack Demonstration

### 🎥 Project Demonstration

Check out the video demonstration below to see the PEN Tool in action!

<div align="center">
  <table>
    <tr>
      <td>
        <a href="https://drive.google.com/file/d/1LyZxGXQPbJabdee5V8nnOsBcqmlk7hgG/view?usp=drive_link">
          <img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/EP%20-%2001.jpg" alt="WiFi Sniffers" height="350"/>
        </a>
      </td>
      <td>
        <a href="https://drive.google.com/file/d/1LyZxGXQPbJabdee5V8nnOsBcqmlk7hgG/view?usp=drive_link">
          <img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/EP%20-%2002.jpg" alt="WiFi Options" height="350"/>
        </a>
      </td>
      <td>
        <a href="https://drive.google.com/file/d/1LyZxGXQPbJabdee5V8nnOsBcqmlk7hgG/view?usp=drive_link">
          <img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/EP%20-%2003.jpg" alt="WiFi Sniffers" height="350"/>
        </a>
      </td>
      <td>
        <a href="https://drive.google.com/file/d/1LyZxGXQPbJabdee5V8nnOsBcqmlk7hgG/view?usp=drive_link">
          <img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/EP%20-%2004.jpg" alt="WiFi Attacks" height="350"/>
        </a>
      </td>
    </tr>
  </table>
</div>

<p align="center">
  <span style="color:#0000FF;"><u><em>Click any thumbnail above to watch the full video on Google Drive.</em></u></span>
</p>

### 📝 Evil Portal Attack: Step-by-Step Procedure

The Evil Portal attack creates a captive portal to harvest user credentials. Here’s how it works:

1️⃣. Launch the Portal: First, the attacker selects 'Evil Portal' under 'WiFi Attacks' on the PEN Tool.

2️⃣. Broadcast a Fake Network: The tool begins broadcasting a fake Wi-Fi network (e.g., "FreeWifi"), which is configured on the SD card. When a user looks for public Wi-Fi, this network appears as a legitimate option.

3️⃣. Redirect to a Fake Page: Once the victim connects, they are automatically redirected to a fake login page, such as a convincing replica of the Facebook login screen.

4️⃣. Capture Credentials: If the user is deceived and enters their credentials (email and password), they are immediately captured by the PEN Tool.

5️⃣. Display and Save: The stolen email and password are then displayed on the PEN Tool's screen and are also saved to the SD card for later access.

---

## 🧩 Offensive & Defensive Activity Demonstration

### 🎥 Project Demonstration

Check out the video demonstration below to see the PEN Tool in action!

<div align="center">
  <table>
    <tr>
      <td>
        <a href="https://drive.google.com/file/d/1yZLyzWDHnHL_NuK_8h7tmuGVCGSQ34g1/view?usp=drive_link">
          <img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/Deauth_attacking.jpg" alt="WiFi Sniffers" width="300" height="400"/>
        </a>
      </td>
      <td>
        <a href="https://drive.google.com/file/d/1yZLyzWDHnHL_NuK_8h7tmuGVCGSQ34g1/view?usp=drive_link">
          <img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/Sniffing.jpg" alt="WiFi Options" width="300" height="400"/>
        </a>
      </td>
      <td>
        <a href="https://drive.google.com/file/d/1yZLyzWDHnHL_NuK_8h7tmuGVCGSQ34g1/view?usp=drive_link">
          <img src="https://github.com/Deshan-Lokuge01/PEN_Tool/blob/main/ScreenShots%20and%20Pictures/Arp%20and%20the%20mac%20of%20Tareget.jpg" alt="WiFi Sniffers" width="300" height="400"/>
        </a>
      </td>
    </tr>
  </table>
</div>

<p align="center">
  <span style="color:#0000FF;"><u><em>Click any thumbnail above to watch the full video on Google Drive.</em></u></span>
</p>

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
  <h3 style="color:orange;">🚧 This project can be further developed with additional features and specifications. 🚧</h3>
  <p><i>Further implementations, improvements, and feature enhancements may be added as development progresses.</i></p>
</div>


<div align="center">
  <h2 style="color: red;">⚠️ Use Only the Authorized Places ⚠️</h2>
</div>

