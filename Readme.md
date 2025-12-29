# Network Traffic Analysis – Terminal-Based Cyber Defense Project

## 📌 Project Overview
This project focuses on **capturing, analyzing, and detecting malicious network activity** using a **terminal-only workflow**.  
The goal is to simulate a **real-world SOC (Security Operations Center)** environment where analysts monitor traffic, identify attack patterns, and respond using IDS tools.

Instead of theoretical learning, this project emphasizes **hands-on traffic inspection, attack detection, and rule-based defense mechanisms**.

---

## 🎯 Objectives
- Capture live network traffic
- Analyze packets to establish normal vs abnormal behavior
- Detect common network attacks (scans, brute force, floods)
- Implement IDS rules for automated threat detection
- Apply enterprise-level (Cisco-style) traffic monitoring logic

---

## 🧠 Problem Breakdown
1. **Traffic Visibility** – Capture raw packets from the network  
2. **Baseline Analysis** – Understand normal network behavior  
3. **Anomaly Detection** – Identify suspicious patterns  
4. **Threat Detection** – Detect active attacks  
5. **Automated Defense** – Generate alerts using IDS rules  

---

## 🛠️ Tools & Technologies
- :contentReference[oaicite:0]{index=0} – Low-level packet capture
- :contentReference[oaicite:1]{index=1} (tshark) – Packet inspection via terminal
- :contentReference[oaicite:2]{index=2} – Signature-based IDS
- :contentReference[oaicite:3]{index=3} concepts – Enterprise traffic monitoring logic

---

## 🖥️ Environment
- OS: Kali Linux / Parrot OS
- Mode: Terminal-based (no GUI dependency)
- Network Interface: Ethernet / Wireless

---

## ⚙️ Installation
```bash
sudo apt update
sudo apt install -y tcpdump wireshark snort tshark
