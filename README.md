# 🛡️Sentinel - Multi-Sensor AI Drone Detection System for Border Surveillance

### Team: Eeshaan Krishna D. · Y. Aditya Reddy · M. Rithwik · P. Vihaan  
**Project Type:** Proof of Concept (PoC)  
**Focus:** Border Security · AI · Sensor Fusion · Embedded Systems  

---

##  Overview

This project aims to design a **multi-sensor, AI-powered drone detection system** that can identify, track, and classify flying objects — such as drones, birds, and kites — in real time.  
The system fuses data from **RF signals, optical and thermal cameras, radar (optional), and acoustic sensors** to provide **accurate and low-latency detection**, even in poor weather or night-time conditions.

---

##  Problem Statement

Small drones are being increasingly used for cross-border spying and smuggling, yet most existing surveillance systems fail to detect them due to their small size, low altitude, and silent operation.  
Our project focuses on creating a **smart, affordable, and modular system** that combines multiple sensors and AI-based analysis to ensure **safer borders and smarter surveillance**.

---

##  Features

- Multi-sensor fusion (camera + RF + thermal + acoustic)  
- AI-powered classification (drone vs bird vs kite)  
- Swarm drone detection and tracking  
- Modular plug-and-play sensor design  
- Real-time alerts with <2s latency (1 km prototype)  
- Scale-up roadmap to 25 km detection range  

---

##  Technical Summary

### Prototype Stage (1 km Range)
- **Camera:** Raspberry Pi Camera or HQ Camera  
- **RF Receiver:** NRF24L01+PA+LNA, RTL-SDR Blog V3  
- **Compute:** Raspberry Pi 5 / Pi Zero 2 W  
- **Power:** 3.7V LiPo battery with TP4056 module  
- **Time Sync:** GPS (PPS-enabled)  
- **Software Stack:**  
  - YOLOv8 for visual detection  
  - CNN/Transformer for RF classification  
  - ROS2 for sensor communication  
  - Kalman Filter + JPDA for multi-object tracking  

### Scale-Up Stage (5–25 km Range)
- **Sensors:** mmWave radar + FLIR thermal camera  
- **Compute:** NVIDIA Jetson Orin/Xavier  
- **Networking:** LoRa / 4G / Mesh for remote nodes  
- **Fusion:** Hybrid AI and statistical model fusion  

---

##  How It Works

1. **Sensors capture data** — RF signals, video frames, temperature, and sound.  
2. **AI models process each sensor stream** individually for detection.  
3. **Fusion algorithm combines results** to generate a unified “object track.”  
4. **Classification module** labels each track as drone, bird, or unknown.  
5. **Alerts are generated** and displayed in the system dashboard.
