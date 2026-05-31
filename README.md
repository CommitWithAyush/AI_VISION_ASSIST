# 👁️ AI Vision Assist

AI Vision Assist is an advanced computer vision and accessibility platform designed to help users understand and navigate their surroundings using Artificial Intelligence.

The system combines real-time object detection, depth estimation, obstacle avoidance, voice feedback, and conversational AI assistance to create a smart visual assistant that can operate through a webcam or camera feed.

---

## 🚀 Features

### 🎯 Real-Time Object Detection
- Detects objects using YOLOv8.
- Displays bounding boxes and confidence scores.
- Supports multiple object classes simultaneously.
- Optimized for both CPU and GPU execution.

### 📏 Distance Estimation
- Estimates the distance of detected objects.
- Provides obstacle proximity information.
- Uses bounding-box analysis and depth estimation techniques.

### 🧠 Depth Estimation
- Powered by MiDaS Depth Models.
- Generates depth maps in real time.
- Helps determine obstacle urgency and navigation decisions.
- Optional depth heatmap visualization.

### 🔊 Voice Guidance System
- Text-to-Speech powered navigation assistance.
- Real-time spoken obstacle warnings.
- Priority-based alert queue.
- Critical alerts override lower-priority messages.

### 🚶 Smart Navigation Assistant
- Detects dangerous obstacles.
- Determines safe movement directions.
- Categorizes warnings into:
  - Critical
  - Warning
  - Informational

### 🎙️ Speech Recognition
- Voice input support.
- Hands-free interaction.
- Accessibility-focused design.

### 🤖 AI Assistant Integration
- Scene understanding.
- Context-aware visual assistance.
- Natural language question answering.
- Conversational interaction based on detected objects.

### 🌐 Backend API
- FastAPI-based architecture.
- WebSocket support for real-time streaming.
- Event-driven communication.
- Frontend integration ready.

### 🖥️ Desktop Interface
- Modern PyQt5 GUI.
- Live camera feed.
- Detection visualization.
- Alert dashboard.
- System statistics monitoring.

### 📡 Ultrasonic Sensor Support
- Optional hardware integration.
- Enhanced obstacle detection.
- Sensor + AI fusion for higher reliability.

---

# 🏗️ System Architecture

```text
Camera Feed
     │
     ▼
YOLOv8 Object Detection
     │
     ├────────► Object Classification
     │
     ▼
MiDaS Depth Estimation
     │
     ▼
Navigation Engine
     │
     ├────────► Distance Estimation
     ├────────► Obstacle Analysis
     ├────────► Safety Assessment
     │
     ▼
Alert System
     │
     ├────────► Voice Guidance
     ├────────► GUI Alerts
     ├────────► AI Assistant
     │
     ▼
User
```

---

# 📂 Project Structure

```text
AI_VISION_ASSIST/
│
├── gui.py
├── obstacle_detection.py
├── obstacle_detection_upgraded.py
│
├── models/
│   ├── yolov8n.pt
│   └── yolov8x.pt
│
├── src/
│   ├── detection.py
│   ├── depth.py
│   ├── navigation.py
│   ├── ranging.py
│   ├── voice.py
│   ├── alerts.py
│   ├── assistant_llm.py
│   ├── speech_input.py
│   └── ultrasonic.py
│
├── server.py
├── requirements.txt
└── README.md
```

---

# ⚙️ Prerequisites

## Hardware Requirements

### Minimum
- Intel i5 / Ryzen 5
- 8GB RAM
- Webcam
- Windows 10/11

### Recommended
- NVIDIA GPU with CUDA support
- 16GB RAM
- Dedicated webcam
- Microphone
- Speakers or headphones

---

# 🐍 Software Requirements

- Python 3.10+
- CUDA Toolkit (Optional)
- Git
- Webcam Drivers

---

# 📦 Installation

## Clone Repository

```bash
git clone https://github.com/CommitWithAyush/AI_VISION_ASSIST.git
cd AI_VISION_ASSIST
```

---

## Create Virtual Environment

### Windows

```bash
python -m venv env
env\Scripts\activate
```

### Linux / Mac

```bash
python3 -m venv env
source env/bin/activate
```

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🧠 Download Models

Create a models folder:

```bash
mkdir models
```

Download YOLO models:

```python
from ultralytics import YOLO

YOLO("yolov8n.pt")
YOLO("yolov8x.pt")
```

Move downloaded files into:

```text
models/
├── yolov8n.pt
└── yolov8x.pt
```

---

# ▶️ Running the Application

## Basic Mode

Lightweight CPU mode.

```bash
python obstacle_detection.py
```

Features:

- YOLO Detection
- Voice Alerts
- Obstacle Detection
- CPU Friendly

---

## Advanced Mode

Full AI Vision Assist Experience.

```bash
python obstacle_detection_upgraded.py
```

Features:

- YOLOv8x Detection
- MiDaS Depth Estimation
- Advanced Navigation
- Voice Guidance
- Depth Visualization

---

## GUI Version

```bash
python gui.py
```

Provides:

- Live Camera Feed
- AI Assistant
- Statistics Dashboard
- Detection Visualization
- Voice Controls

---

## Backend Server

```bash
python server.py
```

Starts:

```text
http://localhost:8000
```

WebSocket Endpoint:

```text
ws://localhost:8000/ws
```

---

# 🎮 Controls

| Key | Action |
|-------|---------|
| Q | Quit Application |
| D | Toggle Depth Overlay |
| H | Toggle Help |

---

# 📡 API Events

## Client → Server

```json
{
  "type": "start"
}
```

```json
{
  "type": "stop"
}
```

```json
{
  "type": "settings"
}
```

```json
{
  "type": "ask"
}
```

---

## Server → Client

```json
{
  "type": "frame"
}
```

```json
{
  "type": "detections"
}
```

```json
{
  "type": "alert"
}
```

```json
{
  "type": "assistant"
}
```

```json
{
  "type": "status"
}
```

---

# 🎯 Use Cases

### Accessibility Assistance
Helping visually impaired users understand surroundings.

### Smart Navigation
Obstacle avoidance and safe movement assistance.

### Educational Projects
Learning computer vision and AI.

### Robotics
Vision module integration.

### Smart Surveillance
Real-time scene monitoring.

### Research
Computer vision experimentation.

---

# 🛠 Technologies Used

- Python
- OpenCV
- YOLOv8
- MiDaS
- PyTorch
- FastAPI
- WebSockets
- PyQt5
- NumPy
- CUDA
- Text-to-Speech
- Speech Recognition

---

# 🔮 Future Improvements

- Mobile Application
- Edge AI Deployment
- Raspberry Pi Support
- Cloud Synchronization
- Multi-Camera Support
- GPS Integration
- Object Tracking
- Facial Recognition
- Emergency SOS System

---

# 👨‍💻 Author

Ayush Kumar Agarwal
Deepak Bhatt
Abhay Srivastav
Karan Singh Dhami
---

# 📄 License

This project is licensed under the MIT License.

---

# ⭐ Support

If you found this project useful:

⭐ Star the repository

🍴 Fork the project

🛠 Contribute improvements

📢 Share with others
