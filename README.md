# Arduino Car: Line Follower & Remote Control 🚗✨

This project was built as part of my **Introduction to Physical Computing** course at **Bezalel Academy of Arts and Design (MA)**.  
It’s a simple Arduino-based car with **two driving modes**:

1. **Self-Driving Line Follower** – the car automatically follows a track using a line sensor.  
2. **Remote Control via Blynk App** – control the car’s movement from a mobile app, with a mode toggle button to switch between self-driving and manual.

---

## 🔧 Hardware & Components
- Arduino board (Uno / compatible)
- ESP8266 Wi-Fi module
- Motor driver (for 2 DC motors)
- Line-tracking sensor
- LED (status indicator)
- Breadboard, jumper wires, power supply

---

## 📱 Software & Libraries
- [Arduino IDE](https://www.arduino.cc/en/software)
- [Blynk](https://blynk.io/) IoT platform & mobile app
- Libraries used:
  - `ESP8266_Lib.h`
  - `BlynkSimpleShieldEsp8266.h`
  - `SoftwareSerial.h`

---

## 🚀 How It Works
- **Line-Following Mode**  
  The car uses a line-tracking sensor to detect black/white contrast and adjusts wheels accordingly.

- **Remote Control Mode (via Blynk)**  
  Buttons in the Blynk app send movement commands (`forward`, `backward`, `left`, `right`) to the Arduino.  
  A **mode button** in the app switches between **self-driving** and **manual**.

---

## 📲 Blynk App Setup
1. Create a new project in the Blynk app.
2. Add:
   - Button widgets for **Forward, Backward, Left, Right** (linked to V7–V10).
   - Mode toggle button (linked to V6).
3. Enter your **auth token** in the Arduino sketch (`#define BLYNK_AUTH_TOKEN`).

---

## ▶️ Getting Started
1. Clone this repo:
   ```bash
   git clone https://github.com/<your-username>/arduino-car.git
   cd arduino-car
2. Open the sketch in Arduino IDE.
3. Update Wi-Fi SSID + password inside the code:
   ```bash
   char ssid[] = "YourNetwork";
   char pass[] = "YourPassword";
4. Upload to your Arduino board.
5. Power the car and start driving!
