# 🛰️ Child Tracking System with BLE, LoRaWAN, and GPS Integration

## 📖 Overview
This project presents a **prototype design and development** of an **IoT-based Child Tracking System** that combines **Bluetooth Low Energy (BLE)**, **LoRaWAN**, and **GPS modules** to enhance child safety through real-time location monitoring and proximity detection.  
It is an upgraded version of a previous GSM-based tracking system, integrating **low-power communication** and **long-range networking** for better performance in both indoor and outdoor environments.

---

## 🎯 Objectives
- To design and implement a **hybrid child tracking system** leveraging BLE, LoRaWAN, and GPS technologies.  
- To enhance real-time **location accuracy**, **communication range**, and **energy efficiency**.  
- To develop an **IoT dashboard or mobile app** for parents and guardians to view live tracking data.  
- To integrate **body detection** and **proximity analysis** for situational awareness around the child.  

---

## 🧩 System Architecture
The architecture consists of the following layers:

1. **Sensing Layer:**  
   - GPS Module → Location data  
   - BLE Module → Proximity and short-range communication  
   - LoRa Module → Long-range data transmission  

2. **Network Layer:**  
   - LoRaWAN Gateway  
   - MQTT/HTTP for data transmission to the cloud  

3. **Application Layer:**  
   - Cloud Server (e.g., ThingsBoard / Firebase / AWS IoT Core)  
   - Android App / Web Dashboard for visualization  

---

## ⚙️ Hardware Components
| Component | Description |
|------------|-------------|
| **ESP32 MCU** | Main microcontroller integrating BLE and Wi-Fi |
| **NEO-6M GPS Module** | Provides real-time location coordinates |
| **RFM95 LoRa Module** | Long-range data communication |
| **Power Supply Unit** | Rechargeable battery (Li-Ion / Li-Po) with voltage regulation |
| **Enclosure** | Compact wearable case (shoe sole / belt attachment) |

---

## 🖥️ Software & Tools
- **Arduino IDE / PlatformIO** – for firmware development  
- **Node-RED / ThingsBoard / Firebase** – for data handling and visualization  
- **Android Studio** – for mobile app integration  
- **Power BI** – for data analytics and reporting  
- **Fritzing / EasyEDA** – for PCB design  

---

## 🔄 Data Flow Diagram
```mermaid
graph TD
A[GPS + BLE Sensor Node] -->|LoRaWAN| B[LoRa Gateway]
B --> C[Cloud Server (MQTT)]
C --> D[Mobile App / Web Dashboard]
