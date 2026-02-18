---

# 🌾 Prototype of Moisture Content Meter in Grain Using ESP32

![Image](https://m.media-amazon.com/images/I/61MDW%2BU%2BrvL.jpg)

![Image](https://europe1.discourse-cdn.com/arduino/original/4X/b/f/5/bf59c155277511be834da260534b8200200ebebe.jpeg)

![Image](https://www.electronicwings.com/storage/PlatformSection/TopicContent/442/icon/ESP32%20Interfacing%20with%20Soil%20Moisture%20Sensor.jpg)

![Image](https://www.electronicwings.com/storage/PlatformSection/TopicContent/442/description/Soil%20Moisture%20Interfacing%20with%20ESP32.jpg)

## 📌 Overview

This project presents a **low-cost, real-time Moisture Content Meter for Grains** using the ESP32 microcontroller and a capacitive moisture sensor.

The system measures moisture levels in grains such as **wheat, rice, and maize**, processes the data using ESP32’s 12-bit ADC, and:

* Displays readings in the **Serial Monitor**
* Automatically segregates grains using a **Servo Motor**
* Logs data to **Google Sheets via Wi-Fi**

This project is developed as a **B.Tech Major Project (ECE – 2025)**.

---

## 🎯 Problem Statement

Traditional grain moisture meters are:

* Expensive
* Non-portable
* Not accessible to small-scale farmers

This project provides a **portable, affordable, and IoT-enabled alternative**.

---

## 🚀 Features

✔ Real-time moisture monitoring
✔ Automatic grain segregation (Accept / Reject)
✔ Google Sheets cloud logging
✔ Wi-Fi enabled (ESP32)
✔ Low-cost hardware (~₹700)
✔ Non-destructive testing
✔ Portable & scalable

---

## 🛠 Hardware Components

* **ESP32 Development Board**
* **Capacitive Soil Moisture Sensor**
* **Servo Motor**
* Breadboard
* Jumper wires
* USB Cable
* Grain samples (Wheat, Rice, Maize)

---

## 🔌 System Architecture

![Image](https://esp32io.com/images/tutorial/esp32-ultrasonic-sensor-servo-motor-wiring-diagram.jpg)

<img width="259" height="194" alt="image" src="https://github.com/user-attachments/assets/f0fe7e68-cf0d-4d59-908f-315fb375e44d" />


![Image](https://dfimg.dfrobot.com/enshop/image/data/BLOG17283/2.jpg)

### Working Flow:

1. Moisture sensor detects dielectric changes in grain.
2. ESP32 reads analog value.
3. Converts raw ADC to moisture percentage.
4. If moisture < threshold → Accept grain.
5. If moisture ≥ threshold → Reject grain.
6. Data is sent to Google Sheets via HTTP request.

---

## ⚙️ Pin Configuration

| Component       | ESP32 Pin |
| --------------- | --------- |
| Moisture Sensor | GPIO 23   |
| Servo Motor     | GPIO 22   |
| Power           | 3.3V / 5V |
| GND             | GND       |

---

## 💻 Software Requirements

* Arduino IDE
* ESP32 Board Package
* Required Libraries:

  * `WiFi.h`
  * `HTTPClient.h`
  * `ESP32Servo.h`

---

## 🌐 Google Sheets Integration

The ESP32 sends data using an HTTP GET request to a deployed Google Apps Script Web App.

Logged Data Includes:

* Date
* Time
* Moisture Percentage
* Servo Angle (Accept/Reject)

---

## 📊 Sample Output

### Serial Monitor Output

```
🌾 Grain Moisture: 42 %
✅ Grain accepted (Low Moisture) → Rotating Left
📤 Sending to Google Sheets...
```

### Moisture Observations

| Grain | Condition | Moisture Level |
| ----- | --------- | -------------- |
| Wheat | Dry       | Low            |
| Wheat | Wet       | High           |
| Rice  | Moist     | Medium         |
| Maize | Wet       | High           |

---

## 📈 Results

* Accurate relative moisture detection
* Real-time response (<5 sec)
* Successful Wi-Fi data logging
* Stable servo-based segregation

---

## 🎓 Educational Value

This project demonstrates:

* Embedded Systems Design
* ADC Data Processing
* IoT Data Logging
* Sensor Calibration
* Smart Agriculture Applications

---

## 🔮 Future Improvements

* OLED/LCD standalone display
* Mobile App integration
* Cloud dashboard analytics
* Multi-sensor support
* Battery/Solar operation
* Grain-specific calibration algorithms

---

## 💰 Cost Estimation

| Component       | Approx Cost |
| --------------- | ----------- |
| ESP32           | ₹450        |
| Moisture Sensor | ₹150        |
| Servo Motor     | ₹120        |
| Misc            | ₹100        |
| **Total**       | **~₹700**   |

---

## 📚 References

* ESP32 Technical Reference Manual – Espressif
* Arduino IDE Documentation
* Capacitive Moisture Sensor Datasheet
* IoT-based Agricultural Research Papers

(Project report reference: )

---

## 👨‍💻 Authors

* S. MD Awaiz
* D. Rahul
* K. Harshavardhan Reddy

Department of Electronics & Communication Engineering
KLEF, Hyderabad
2025

---

## ⭐ If you like this project

Give it a ⭐ on GitHub and feel free to fork or improve it!

---
