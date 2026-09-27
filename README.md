# 🚗BrakeSense-AEB

Smart Obstacle Detection & Automatic Emergency Braking System

BrakeSense-AEB is an Arduino-based vehicle safety prototype that detects obstacles using a distance sensor, provides multi-stage visual and audio warnings, and automatically stops the motor when an obstacle reaches a critical distance.

---

## 🎯 Objective

The main objective is to create a simple, low-cost safety system that can:

- Detect obstacles ahead
- Warn the driver before a collision
- Provide visual and audio alerts
- Automatically stop the motor during critical situations
- Improve overall vehicle safety

---

## ⚙️ How It Works

The system continuously measures the distance between the sensor and the obstacle in front of the vehicle. Based on the detected distance, the system operates in three different safety zones.

🟢 Safe Zone — More Than 36 cm

When the detected obstacle is more than 36 cm away, the system considers the situation safe. The stepper motor continues running, allowing the vehicle to move forward normally. The Green LED remains ON, indicating the safe condition, and the buzzer remains silent.

🟡 Warning Zone — 16 cm to 36 cm

When an obstacle is detected between 16 cm and 36 cm, the system enters the warning zone. The stepper motor continues running, but the Yellow LED turns ON to indicate potential danger. At the same time, the buzzer produces a low-frequency warning sound to alert the driver that an obstacle is getting closer.

🔴 Critical Zone — Less Than 16 cm

When the obstacle comes within 16 cm, the system considers the situation critical. The stepper motor immediately stops and the automatic emergency braking mechanism is activated. The Red LED turns ON, and the buzzer produces a high-frequency and louder alert sound to indicate an imminent collision.

🛑 Emergency Braking

The automatic braking mechanism is designed to stop the vehicle when the detected obstacle reaches the critical distance. This allows the system to react automatically instead of depending entirely on the driver's response time.

🔊 Alert System

The project uses different LED indicators and buzzer frequencies to communicate the current safety condition. Green represents a safe condition, yellow indicates a warning, and red represents a critical emergency condition.

Overall, the system continuously monitors the surroundings, warns the driver when necessary, and automatically stops the motor when a collision becomes imminent.

---
## ✨ Key Features

- 📡 Real-time obstacle detection
- 🟢🟡🔴 Three-stage warning system
- 🔊 Variable-frequency buzzer alerts
- 🛑 Automatic emergency braking
- ⚙️ Stepper motor control
- 💰 Low-cost hardware
- 🔌 Arduino-based embedded system

---

## 🛠️ Components Required

▪ Arduino Uno  
▪ Distance Sensor (HC-SR04)  
▪ Buzzer  
▪ Green LED  
▪ Yellow LED  
▪ Red LED  
▪ A4988 Stepper Motor Driver  
▪ Stepper Motor  
▪ 3 × Resistors  
▪ Breadboard  
▪ Jumper Wires

---

## 💻 Technology Used

- Microcontroller: Arduino Uno
- Programming Language: C++
- Development Environment: Arduino IDE
- Motor Driver: A4988
- Distance Sensor: Ultrasonic Sensor
- Motor: Stepper Motor

---

## 🔄 System Flow

             START
               │
               ▼
       Read Sensor Distance
               │
               ▼
       ┌─────────────────┐
       │ Distance > 36cm │
       └────────┬────────┘
                │
             YES│
                ▼
          🟢 SAFE ZONE
       Motor → ON
       Green LED → ON
       Buzzer → OFF
                │
                │ NO
                ▼
       ┌─────────────────┐
       │ 16cm – 36cm     │
       └────────┬────────┘
                │
             YES│
                ▼
        🟡 WARNING ZONE
       Motor → ON
       Yellow LED → ON
       Buzzer → LOW
                │
                │ NO
                ▼
       🔴 CRITICAL ZONE
       Motor → OFF
       Brake → ON
       Red LED → ON
       Buzzer → HIGH

---

### 🚀 Future Improvements

- Multiple sensors for wider obstacle detection
- Speed-dependent braking
- OLED/LCD distance display
- Camera-based obstacle detection
- IoT-based monitoring
- GPS accident/location tracking
- Mobile application integration

---

### 📌 Applications

This project can serve as a prototype for:

- 🚗 Smart vehicle safety systems
- 🤖 Autonomous robots
- 🛺 Low-speed autonomous vehicles
- 🏭 Industrial safety vehicles
- 🎓 Embedded systems projects

---

### 👥 Contributors

This project was developed by:

1. Arka Chakraborty
2. Arnab Paul
3. Deep Mondal
4. Adarsh Kumar Sah
5. Subhankar Dawn

---

### 📄 Project Information

- Project Name: BrakeSense-AEB
- Full Name: Smart Obstacle Detection & Automatic Emergency Braking System
- Project Type: Arduino-Based Embedded System
- Programming Language: C++
- Microcontroller: Arduino Uno
- Sensor: HC-SR04 Ultrasonic Distance Sensor
- Motor Driver: A4988 Stepper Motor Driver
- Motor: Stepper Motor
- Alert System: Green, Yellow & Red LEDs with Buzzer
- Detection Method: Real-Time Distance Measurement
- Braking Method: Automatic Emergency Braking
- Development Platform: Arduino IDE
- Main Purpose: Vehicle Safety and Collision Prevention
- Application: Smart Vehicle Safety System
- Project Status: Working Prototype

#### «⚠️ Note: This is an educational prototype. It should not be directly installed in a real vehicle as a safety-critical braking system without automotive-grade hardware, redundancy, testing, and certification.»

