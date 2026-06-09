
# 🚦 Smart Traffic Signal System

An AI-powered traffic management system that uses Computer Vision and Reinforcement Learning to dynamically control traffic signals based on real-time traffic conditions.

The system combines YOLOv8 for vehicle detection, DeepSORT for vehicle tracking, and a DQN-based Reinforcement Learning agent to optimize traffic light timing and reduce congestion.

---

## 📌 Project Overview

Traditional traffic lights rely on fixed timers and cannot adapt to changing traffic conditions. This often leads to:

- Increased vehicle waiting time
- Traffic congestion
- Fuel wastage
- Higher CO₂ emissions

This project introduces an intelligent traffic signal system that monitors vehicle density in real time and adjusts traffic signals dynamically to improve traffic flow and intersection efficiency.

---

## 🎯 Objectives

- Detect vehicles using Computer Vision
- Track vehicles across video frames
- Measure lane density and waiting time
- Apply Reinforcement Learning for decision making
- Reduce traffic congestion
- Improve vehicle throughput
- Minimize fuel consumption and emissions

---

## 🏗️ System Architecture

```text
Traffic Camera Feed
        │
        ▼
 YOLOv8 Vehicle Detection
        │
        ▼
 DeepSORT Tracking
        │
        ▼
 Lane Assignment & Density Calculation
        │
        ▼
 Reinforcement Learning Agent (DQN)
        │
        ▼
 Traffic Signal Controller
        │
        ▼
 Optimized Signal Timing
```

---

## ⚙️ Workflow

### 1. Data Acquisition
- Capture live traffic video streams using cameras.

### 2. Vehicle Detection
- Detect vehicles using YOLOv8.
- Identify cars, trucks, buses, and motorcycles.

### 3. Vehicle Tracking
- Assign unique IDs using DeepSORT.
- Prevent duplicate counting.

### 4. Density Estimation
- Calculate lane occupancy and queue density.

### 5. Decision Making
- RL Agent receives the current traffic state.
- Selects the optimal action.

### 6. Signal Control
- Extend the green phase.
- Switch traffic signal phases when necessary.

---

## 🧠 Reinforcement Learning Model

### State

The agent observes:

- Queue length per lane
- Total waiting time
- Current signal phase

### Actions

- Extend current green signal
- Switch to another phase

### Reward

Positive reward:
- Reduced waiting time
- Increased throughput

Negative reward:
- Long queues
- Frequent unnecessary signal changes

---

## 🔍 Vehicle Counting Strategy

The project initially used ID-based counting through DeepSORT.

To improve accuracy during heavy traffic and occlusion scenarios, a Density-Based ROI method was introduced.

### Advantages

- Better handling of occlusion
- More accurate traffic density estimation
- Improved performance during traffic jams
- Lower processing overhead

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|----------|
| Python | Main programming language |
| YOLOv8 | Vehicle detection |
| DeepSORT | Vehicle tracking |
| OpenCV | Image processing |
| Reinforcement Learning | Traffic signal optimization |
| DQN | RL algorithm |
| SUMO | Traffic simulation |
| PyTorch | Deep learning framework |
| Jupyter Notebook | Training & experiments |
| VS Code | Development |
| GitHub | Version control |

---

## 📁 Project Structure

```text
Smart-Traffic-Signal-System/
│
├── models/
│   ├── yolov8/
│   └── dqn/
│
├── videos/
│
├── results/
│
├── simulations/
│
├── notebooks/
│
├── src/
│   ├── detection/
│   ├── tracking/
│   ├── counting/
│   ├── rl_agent/
│   └── controller/
│
├── requirements.txt
├── main.py
└── README.md
```

---

## 📊 Results

| Metric | Traditional System | AI System | Improvement |
|----------|----------|----------|----------|
| Average Waiting Time | 45.2 s | 28.5 s | 37% Reduction |
| Vehicle Throughput | 120 cars/hour | 165 cars/hour | 38% Increase |
| Max Queue Length | 18 Vehicles | 7 Vehicles | 61% Reduction |
| CO₂ Emissions | High | Optimized | Significant Reduction |

---

## 🚗 Demo

(view the demo)[https://smart-signal-system.github.io/Smart-traffic-signal-system-/]

---

## 🚀 Future Work

- Emergency vehicle prioritization
- Multi-intersection coordination
- Smart city integration
- Real-world deployment
- Edge AI optimization
- Vehicle-to-Infrastructure (V2I) communication

---

## 👥 Team Members

- Cristina Hossam Sadeq
- Noreen Adel Saad
- Merit Saad Shafik
- Mariam Hanafi Mahmoud
- Hassna Magdy Gaber
- Mariam Atef Refaat
- Yara Hassan Hasanein
- Yassin Salah Eldin

---

## 👨‍🏫 Supervision

### Academic Supervisor
**Prof. Alaa El-Deen Abd ElHakim**  
Professor, Department of Electrical Engineering  
Faculty of Engineering, Assiut University

### Teaching Assistant
**Eng. Eman Tamam**

---

## 📚 References

- YOLOv8
- DeepSORT
- DQN
- SUMO
- OpenCV
- PyTorch
- Intelligent Traffic Signal Control Research

---

## 📜 License

This project was developed as a Work-Based Project at Sphinx University, Faculty of Computers and Artificial Intelligence (2025/2026).

