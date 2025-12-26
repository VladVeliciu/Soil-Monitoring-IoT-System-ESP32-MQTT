# Soil Quality Sensor – IoT System (ESP32 + RS485 + Raspberry Pi)

IoT system for real-time **soil quality monitoring**, developed during an Erasmus internship (Universitat de València, Jul–Sep 2023).  
Reads **7 parameters** from an industrial RS485 soil sensor and sends data via **MQTT** to a local ThingsBoard server running on Raspberry Pi.

**Measured parameters:**
Nitrogen (N), Phosphorus (P), Potassium (K), pH, Moisture, Temperature, Electrical Conductivity.

### System Architecture
- **ESP32-S3** → reads RS485 sensor via **MAX3483** transceiver  
- MQTT over Wi-Fi → **Raspberry Pi 4** (access point + Docker + ThingsBoard)
- Live dashboard: charts, widgets & historical logs (local network)

### Hardware & PCB
- Custom PCB designed in **Altium Designer** for ESP32 + MAX3483 + connectors  
- Includes: schematics, footprints, routing, design rules, Gerber & drill files
- Board validated through DRC and exported for fabrication  
*(PCB photos & 3D model available in repository)*

### Repository contents
- `final_code.ino` → ESP32 firmware (Arduino IDE)
- PCB files: Gerbers, NC Drill, BOM, schematics
- `Report.pdf` → system report (data flow, MQTT config, dashboard)
- `Report-PCB.pdf` → PCB design report (rules, routing, 3D)
- `Comparison with other approaches.pdf` → literature review (IoT/WSN)

### Tech stack
ESP32-S3, RS485 / MAX3483, Arduino C++, MQTT, ThingsBoard, Docker, Raspberry Pi, Altium Designer

---

## Highlights
- Full IoT system from sensor → edge device → server → dashboard  
- Stable communication using **serial data parsing + byte frame validation**  
- Dashboard for real-time display and remote monitoring  

---

## 👤 Developed by
**Vlad Veliciu & Victor Mihaiu** — Erasmus Research Internship, Universitat de València (Spain)  
