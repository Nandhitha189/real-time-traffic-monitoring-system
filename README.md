# IoT Smart Traffic Monitoring System

## Overview
This project is a real-time traffic monitoring system using an ESP32 client and a Python UDP server. The ESP32 simulates lane-wise vehicle counts and sends data through UDP. The Python server receives the data, aggregates traffic state, detects congestion, identifies the most congested lane, checks intersection overload, and measures packet throughput.

## Features
- ESP32-based UDP client
- Python UDP server
- Lane-wise vehicle count transmission
- Real-time traffic data aggregation
- Congestion detection per lane
- Intersection overload alert
- Most congested lane identification
- Throughput calculation in packets per second

## System Architecture
- ESP32 Client: Simulates lane-wise vehicle count data
- UDP Protocol: Sends lightweight real-time packets
- Python Server: Receives, aggregates, and analyzes traffic data
- Analytics Logic: Detects congestion, overload, and throughput

## Key Highlights
- Real-time IoT communication using UDP
- Combines embedded systems with server-side analytics
- Demonstrates smart city traffic monitoring logic
- Includes packet throughput measurement

## Tech Stack
- ESP32
- Arduino C/C++
- Python
- UDP Socket Programming
- IoT Networking

## Project Structure
```text
esp32_client/
  esp32_client.ino
python_server/
  server.py
README.md
```

## How to Run
### 1. Start the Python Server
```bash
cd python_server
python server.py
```

### 2. Configure ESP32 Client
In `esp32_client.ino`, update:
```cpp
const char* ssid = "YOUR_WIFI_NAME";
const char* password = "YOUR_WIFI_PASSWORD";
const char* udpAddress = "YOUR_SERVER_IP";
```

### 3. Upload to ESP32
Upload the `.ino` file using Arduino IDE.

## Message Format
```text
Lane=NORTH,Vehicles=25
```

## My Contributions
- Built the UDP communication flow between ESP32 and Python server.
- Implemented lane-wise aggregation and congestion detection logic.
- Added overload detection based on total intersection vehicle count.
- Added throughput monitoring to evaluate packet rate.

## Learning Outcome
This project helped me understand IoT communication, UDP networking, real-time data aggregation, and smart city traffic monitoring logic.
