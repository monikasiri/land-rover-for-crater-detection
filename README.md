### **Project Summary**
---
This project is about building a solar-powered land rover that detects craters in real-time using a CNN-based deep learning model. The camera captures images and the model predicts whether the surface is crater or not. The rover's behavior is determined based on this prediction. Fing is used for IP scanning to access the web interface.

### **Abstract**
---
A Raspberry Pi-based rover runs a CNN model to detect crater from live camera input. Upon detection, a decision is made to move or stop. A Flask-based web app allows users to upload images and receive predictions. Fing helps locate the Raspberry Pi's IP for access.

### **Introduction**
---
The rover uses a webcam and Raspberry Pi to detect dusty surfaces. The model is pre-trained and loaded during runtime. If the uploaded or live-captured image is dusty, the prediction is shown with confidence. A local Flask app provides an interface for image upload and result display.(dusty-crater present,non-dusty-crater is not present)

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
- Fing (Network device discovery)

### **Python Libraries Used**
---
- Python 3.x  
- TensorFlow  
- OpenCV  
- Flask  
- NumPy  
- PIL  
- os, time, webbrowser

### **Algorithm Used**
---
- CNN model processes 128x128 RGB images  
- Outputs prediction with confidence score  
- Trained using Adam optimizer and cross-entropy loss

### **How It Works**
---
1. Camera captures frame or user uploads an image.  
2. Image is resized to 128x128 and normalized.  
3. CNN model loads using TensorFlow and restores saved graph.  
4. Image passed to model, which predicts "dust" or "non-dust".  
5. Output displayed via Flask web interface.  
6. Fing is used to find the Raspberry Pi's IP for web access.
