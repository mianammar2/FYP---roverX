# IPath Finder 🚀  
**An Intelligent Rover for Autonomous Terrain Navigation**

## 📌 Overview
IPath Finder is an autonomous rover inspired by NASA's Sojourner mission. Designed for rugged terrain navigation and real-time environmental interaction, the rover combines **AI**, **ROS 2**, **solar energy**, and **modular hardware** to deliver a sustainable, affordable solution for research, education, and disaster response.

---

## 👨‍💻 Team
- **Muhammad Ammar**  
  BSCS (2021–2025), University of South Asia  
  Roll No: B-26257  
  Supervisor: Mr. Taib Ali

---

## 🎯 Project Objectives
- Real-time obstacle detection and avoidance  
- Self-navigation using GPS & IMU with sensor fusion  
- Terrain mapping using camera + vision AI (TensorFlow Lite)  
- Auto-aligning solar panels for efficient energy harvesting  
- Manual override using MQTT-based remote control  
- Data logging and remote visualization with Node-RED & Grafana  

---

## 🔧 Tools & Technologies

### Hardware:
- Raspberry Pi 4 (8GB), Arduino UNO  
- NoIR Pi Camera, Ultrasonic Sensors, IR Sensors  
- Solar Panel with LDR-based Tracking  
- Motor Drivers (L298N), GPS Module, Li-Ion Battery  

### Software:
- **ROS 2 (Humble)**  
- Python 3.8+, OpenCV, TensorFlow Lite  
- Ubuntu 22.04 / Raspberry Pi OS  
- MQTT, InfluxDB, Node-RED  
- Arduino IDE  

---

## 📐 Architecture
The system is built modularly with:
- **Sensor Nodes** (camera, ultrasonic, GPS, IMU)  
- **Control Nodes** (motor drivers, servos)  
- **Perception Nodes** (vision AI, sun tracking)  
- **Communication Layer** (MQTT, ROS 2 topics)  
- **Mission Manager** (waypoint navigation, obstacle avoidance)

---

## ✅ Features

| Feature                    | Description                                             |
|---------------------------|---------------------------------------------------------|
| Autonomous Navigation     | GPS + IMU + obstacle sensing + path planning           |
| Obstacle Avoidance        | Ultrasonic sensors + real-time rerouting               |
| Solar Tracking System     | LDR sensors adjust panel angles automatically          |
| Manual Override           | MQTT-based manual remote control from UI               |
| Data Dashboard            | Telemetry visualized with Node-RED + Grafana           |
| Real-Time Video           | MJPEG streaming via NoIR Pi camera                     |
| Modular ROS Design        | Easy to expand, debug, and maintain                    |

---

## 🧪 Test Cases
- **Camera Initialization**  
- **Object Detection**  
- **Motor & Servo Commands**  
- **Obstacle Avoidance**  
- **Sun Tracking System**  
- **Remote Control via MQTT**

---

## 📊 Development Stats
- **Estimated LOC**: 4,500  
- **Effort**: ~22 Person-Months  
- **Time to Completion**: ~7 months  
- **Estimated Cost**: Rs. 2,74,000  

---

## 📅 Timeline
- **Planning & Design** – Jan 2025  
- **Development** – Feb–Apr 2025  
- **Testing & Implementation** – May–Jun 2025  
- **Presentation & Documentation** – Jul 2025  

---

## 🧠 Future Improvements
- Add Soil Testing Module (pH, moisture)  
- Add Wireless Docking / Charging  
- Enable AI-Based Terrain Classification  
- Integration with LoRa for long-range communication  

---

## 📄 License
This project is developed for academic and research use only. All third-party libraries are used under open-source licenses.

---

## 🤝 Acknowledgements
Special thanks to **Mr. Taib Ali** for guidance, and to the University of South Asia for providing the platform to explore intelligent robotics in a real-world context.

---

## 📬 Contact
**Muhammad Ammar**  
📧 [Insert email]  
🌐 [LinkedIn or GitHub if available]

