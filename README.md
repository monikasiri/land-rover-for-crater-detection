### **Project Summary**
---
A solar-powered autonomous rover that uses a CNN model to detect craters in real-time and makes movement decisions using IoT communication. The system is designed for remote terrains like space or disaster areas.

### **Abstract**
---
This project combines deep learning, IoT, and renewable energy to create a smart rover capable of environmental awareness. The CNN model classifies camera input as crater or non-crater. Based on the result, the rover stops or moves using commands sent via IoT to an Arduino-based control system.

### **Introduction**
---
Navigating unknown terrain requires real-time hazard detection. This system uses a Raspberry Pi for image processing, a CNN for crater classification, and Arduino for motor control. IoT connectivity allows real-time human monitoring.

### **Hardware Used**
---
- 200RPM 12Volts DC Motor
- L298 2A Dual Motor Driver Module With PWM Control
- Zebronics Zeb-Crystal Pro Web Camera with USB Powered, 3P Lens
- Lead Acid Battery
- Power Bank for Raspberry Pi
- Solar Charge Controller
- Raspberry Pi 4

### **Software Used**
---
- Fing (Network device discovery and IP scanning)

### **Algorithm Used**
---
- CNN with convolution, pooling, flatten, dense, and sigmoid layers
- Binary classification: crater vs. non-crater
- Input image: 64x64 RGB
- Output: 0 (non-crater) or 1 (crater)

### **How It Works**
---
1. Raspberry Pi captures image from camera
2. Image is resized, normalized, and fed to CNN
3. CNN outputs prediction
4. If crater → send 'STOP' command to Arduino via IoT
5. If non-crater → send 'FORWARD' command
6. Arduino executes motor control based on received signal
