# IoT-Controlled Boat using ESP32 and Blynk

## Overview
This project demonstrates an IoT-based, mobile-controlled boat using the **ESP32-WROVER** development board and the **Blynk** platform. The boat is navigated in real-time using a smartphone app, enabling control over direction and speed through a Wi-Fi connection.

This project blends **embedded systems**, **wireless communication**, and **motor control** into a fully functional remote-controlled prototype.

---

## Hardware Components
- **ESP32-WROVER** development board  
- **L298N Motor Driver** (to drive two DC motors)  
- **2 × DC Motors** (for forward/reverse propulsion)  
- **Servo Motor** (for rudder/steering)  
- **2 × 18650 Li-Ion Batteries** (7.4V total supply)  
- **Buck Converter / Voltage Regulator** (for ESP32)  
- **Breadboard, jumper wires, toggle switch**  
- **Plastic chassis (e.g., Pepsi bottle) for buoyancy**  
- **Waterproofing** (sealant, hot glue, tape)

---

## Software & Tools
- **Arduino IDE** (for ESP32 programming)  
- **Blynk App** (for mobile control interface)  
- **Blynk Auth Token** (to connect ESP32 to your Blynk account)  
- **ESP32 Board Package** for Arduino

---

## Functional Description
- Two DC motors are used for propulsion and speed control, driven via L298N.
- A servo motor controls the rudder for left/right steering.
- The Blynk app sends commands via Wi-Fi to the ESP32, which adjusts motor speeds and direction accordingly.
- The project includes battery regulation, power management, and connectivity handling for real-world conditions.

---

## Challenges & Solutions
| Challenge                      | Solution |
|-------------------------------|----------|
| Wi-Fi disconnects             | Used strong signal / mobile hotspot and ensured correct auth token |
| ESP32 resetting on load       | Added bulk capacitor to servo supply and regulated power properly |
| Motor direction reversed      | Swapped wiring and corrected logic in code |
| Blynk controls unresponsive   | Fixed widget pin mapping and code handling |
| Water leakage                 | Sealed chassis and motor housing with glue gun |
| Short battery runtime         | Used 2 × 18650 rechargeable cells and monitored voltage |

---

## Blynk Interface
- **Joystick Widget**: Controls direction (servo)  
- **Buttons/Sliders**: Control speed (PWM signal)  
- **Virtual Pins**: Mapped to GPIO for clean abstraction

---

## How to Use
1. Upload the Arduino code to your ESP32 using Arduino IDE.  
2. Connect motor and servo wires as per pin configuration.  
3. Open the Blynk app and use your project token.  
4. Control the boat wirelessly via your smartphone!

---

## Learning Outcomes
- Embedded control using **ESP32**  
- Mobile app integration with **Blynk IoT**  
- Real-time control of motors and actuators  
- Practical debugging in hardware systems (power, communication, timing)

---

## Author
**Sarath Srinivasan**  
B.Tech Electrical Engineering | Passionate about IoT, Embedded Systems & Robotics

---

## Tags
`IoT` `ESP32` `Blynk` `Motor Control` `Embedded Systems` `Robotics` `Wi-Fi` `Mobile App`
