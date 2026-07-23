# Layer 2 Switch Simulator with Error Detection & Network Analysis

## 📌 Project Overview
This project is a software-based simulation of a **Layer 2 Ethernet Switch** (Learning Bridge). It is designed to demonstrate core networking concepts such as MAC address learning, frame forwarding, flooding, and error detection using CRC/Checksum. Furthermore, it integrates a **Data Analysis module** that logs network traffic and visualizes switch performance.

## 🏛️ Architecture & Design
The switch is built using Python's **Object-Oriented Programming (OOP)**. 
Why `Thread` and `Queue`?
- **Concurrency Simulation:** Each port on the switch acts as an independent entity. We use `threading` to simulate multiple ports receiving and processing frames simultaneously.
- **Asynchronous Handling:** `queue.Queue` is used to buffer incoming frames, ensuring that the switch doesn't miss packets while processing a previous one. This mimics the hardware buffers in real network switches.

## ⚙️ Implemented Mechanisms
1. **Self-Learning (MAC Table):** The switch dynamically learns the source MAC addresses of incoming frames and maps them to the incoming port.
2. **Forwarding & Flooding:** 
   - If the destination MAC is known, the frame is forwarded **exclusively** to the destination port (reducing network congestion).
   - If the destination is unknown, the frame is **flooded** to all ports except the incoming one.
3. **Error Detection (CRC/Checksum):** Each frame includes a checksum. The switch verifies this checksum and drops any corrupted frames, mimicking the data integrity checks in Ethernet.
4. **TTL (Time-To-Live) Mechanism:** Implemented to prevent broadcast storms in potential loop scenarios.

## 📊 Data Analysis & Visualization
This project includes a powerful data analysis module (`NetworkLogger`). 
The switch logs all events to a `network_logs.csv` file. 
You can run the `analyze_switch.py` script to generate statistical insights and graphs.

## 🛠️ Technologies Used
- **Language:** Python 3.x
- **Libraries:** `threading`, `queue`, `csv` (for simulation), `pandas`, `matplotlib` (for analysis).
- **Future Upgrade:** `scapy` integration for real packet sniffing.

## 🚀 How to Run
1. Clone the repository.
2. Install required dependencies (if not already installed):
   ```bash
   pip install pandas matplotlib
3. Run the main simulation:
   ```bash
    python switch_simulator.py
4. (Opional) Run the Analysis:
   ```bash
     python analysis_switch.py
5. Check the generated network_logs.csv and switch_analysis.png.

## 📝 Project Report (LaTeX)
A comprehensive academic report detailing the architecture, code logic, and test results is available in the /report folder (compiled to PDF) - To be added.
