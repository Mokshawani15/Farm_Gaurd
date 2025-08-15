# Farm_Gaurd
# 🚜 Farm Security System – AI-Powered Real-Time Animal Detection & Response

## Overview
This **Farm Security System** is a prototype developed to demonstrate the feasibility of integrating **real-time video analysis** with **automated response mechanisms** for farm protection.  

While functional, this prototype is **not intended for large-scale deployment** but instead showcases the **core concepts** of hardware-software integration for detecting and deterring animals from entering farm areas.

---

## System Overview
The system consists of two main components:

### **1. Hardware Module**
- **ESP8266 Microcontroller** – Acts as the main IoT device for hardware control and communication.
- **Stepper Motor** – Rotates the camera/mobile phone for wider surveillance coverage.
- **Buzzer & LED** – Provide audible and visual alerts when animals are detected.
- **Mobile Phone** – Serves as a webcam for video capture.
- **Motor Driver (L298N)** – Controls stepper motor movement.

### **2. Software Module**
- Runs on **Raspberry Pi** or **PC**.
- Uses **OpenCV** for video frame processing.
- Employs a **pre-trained machine learning model** for animal detection.
- Communicates with the ESP8266 via **HTTP requests**.
- Sends **real-time alerts** to the farmer through **Telegram**.

---

## Prototype Workflow
1. **Video Capture**  
   - Mobile phone streams live video to a **local server**.
   
2. **Animal Detection**  
   - Raspberry Pi or PC processes video frames using **OpenCV**.
   - Pre-trained classifier identifies animals such as **deer**.
   
3. **Signal Transmission**  
   - On detection, system sends an **HTTP request** to ESP8266.
   
4. **Responsive Actions**  
   - ESP8266 activates buzzer & LED.
   - Stepper motor rotates the camera to track movement.
   - Sends **Telegram notification** to the farmer.

---

##  Limitations of the Prototype
- **Simulated Testing Environment** – Detection accuracy may be affected in real-world conditions due to lighting, weather, or animal behavior.
- **Basic Hardware Setup** – Requires durability upgrades for outdoor farm use.
- **Wi-Fi Dependency** – May not be reliable in remote farm areas without strong connectivity.

---

## System Design

### **Hardware Architecture**
- **ESP8266 Microcontroller** – Core IoT control unit.
- **Stepper Motor** – Provides rotational camera coverage.
- **L298N Motor Driver** – Controls motor operation.
- **Buzzer & LED** – Alert mechanisms.
- **Mobile Phone** – Streams video to processing unit.

**Wiring Diagram (Conceptual)**:
- ESP8266 → L298N → Stepper Motor
- ESP8266 GPIO → Buzzer & LED
- Mobile phone connects via **local network** to processing unit.

---

### **Software Architecture**

#### **1. Animal Detection Module** (PC/Raspberry Pi)
- Captures live video feed using **OpenCV**.
- Processes frames with a **trained ML model**.
- Detects animals and sends **HTTP requests** to ESP8266.

#### **2. Hardware Control Module** (ESP8266)
- Listens for HTTP commands from the detection system.
- Activates buzzer, LED, and rotates stepper motor.
- Sends alerts to farmer via **Telegram API**.

---

## Tech Stack
- **Hardware:** ESP8266, Stepper Motor, L298N Motor Driver, Buzzer, LED, Mobile Phone
- **Programming Languages:** Python, C++
- **Libraries & Frameworks:** OpenCV, TensorFlow/Keras (for ML model)
- **Communication Protocols:** HTTP, Wi-Fi
- **Alert System:** Telegram Bot API

---

# Flash ESP8266 with control code
# (Use Arduino IDE or PlatformIO)
