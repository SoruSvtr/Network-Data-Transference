# Network Traffic Analysis with Python & Scapy

This project focuses on capturing, analyzing, and visualizing network traffic using real-world scenarios. It combines the power of **Wireshark** for packet capture and **Python (with Scapy and Matplotlib)** for automated statistical analysis, protocol classification, and visualization.

## 📖 Overview

The project demonstrates a complete "Capture -> Analyze -> Visualize" pipeline. We analyzed several key network protocols by simulating real user actions (e.g., web browsing, DNS resolution, ping) and processing the generated `.pcapng` files programmatically.

### Scenarios Analyzed:
- **DNS Query:** Using UDP (Port 53) to resolve domain names.
- **TCP Handshake:** Analysis of the 3-Way Handshake (SYN, SYN-ACK, ACK).
- **HTTP Traffic:** High-volume web browsing and content downloading (via CDN).
- **ICMP:** Ping request/reply analysis.
- **ARP Broadcast:** Simulating a local network discovery using a custom crafted packet.

## 🛠️ Technologies Used
- **Python 3.8+** (Core programming language).
- **Scapy** (For reading `.pcapng` files and crafting custom packets).
- **Matplotlib** (For generating pie charts and bar charts).
- **Wireshark** (For capturing live network traffic).
- **Counter (Collections)** (For statistical aggregation of IPs and Protocols).

## 📂 Project Structure
    ```bash📁 
    Project 4/
    │
    ├── 📄 ProjectDT.pdf                 # Complete project report (in Persian)
    ├── 📄 final_code.py                 # Main Python script for reading & analyzing .pcapng files
    ├── 📄 bm.py                         # Python script to craft and send an ARP Broadcast packet
    │
    ├── 📁 packets/                      # Folder containing the raw captured traffic files
    │   ├── dns_capture.pcapng
    │   ├── tcp_capture.pcapng
    │   ├── http_capture.pcapng
    │   ├── icmp_capture.pcapng
    │   └── arp_capture.pcapng
    │
    └── 📁 charts/                       # Generated visualization outputs
    ├── chart_DNS.png
    ├── chart_TCP_TLS.png
    └── chart_HTTP.png
## 🚀 How to Run the Analysis
1. Install dependencies: (if not intalled yet)
    ```bash
    pip install scapy matplotlib
2. Run the main analyzer:
   ```bash
   python3 final_code.py
3. (Optional) Run the ARP broadcast simulator:
   ```bash
   python3 bm.py

## 👥 Contributors
Soroush Maleki
Ali Aghabarrari Kazemi

## 📝 License
This project is created for academic purposes as part of the "Data Transmission" course at University of Mazandaran.
