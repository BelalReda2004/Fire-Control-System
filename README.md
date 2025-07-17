# 🔥 Fire Control System using Arduino

## 📖 Project Overview
This project presents a **smart fire detection and alert system** powered by an **Arduino Nano**, capable of monitoring ambient temperature using an **NTC thermistor**. Based on predefined temperature thresholds, the system provides **visual alerts (LCD & LED)** and **audible warnings (buzzer)** to signal fire-like conditions.

It’s a low-cost, efficient solution suitable for **educational, residential, and small industrial safety applications**.

---

## 🧰 Components Used

| Component                     | Description                                              |
|------------------------------|----------------------------------------------------------|
| 🧠 Arduino Nano              | Main controller managing all logic and components        |
| 🌡️ NTC Thermistor           | Temperature sensor for detecting heat/fire conditions    |
| 🖥️ 16x2 LCD Display         | Displays current temperature and warning messages        |
| 🔊 Buzzer                   | Emits alert tones based on system state                  |
| 🔴 Red LED                  | Visual indicator for critical fire conditions            |
| 🎚️ Potentiometer            | Controls contrast of LCD display                         |
| 🔌 Breadboard & Jumper Wires | Circuit assembly and connectivity                        |
| 🔩 Resistors                 | Used for voltage divider and LED current protection      |
| 🔋 Power Source              | USB or external source to power the system               |

---

## ⚙️ How It Works

### 🔸 Normal Mode
- Temperature is within safe limits (`< 45°C`)
- LCD displays real-time temperature
- Buzzer and LED are OFF

### ⚠️ Warning Mode
- Temperature between **45°C and 65°C**
- LCD shows: `"Warning: FIRE!"`
- Buzzer emits **intermittent beeps**

### 🚨 Critical Mode
- Temperature exceeds **65°C**
- LCD displays: `"Run away now!!"`
- Buzzer emits **continuous urgent tone**
- Red LED turns ON

---

## 🧠 System Logic

The system processes temperature readings from the thermistor using a **voltage divider circuit**, then classifies the situation into three levels:

| Mode           | Temperature Range | System Response                                      |
|----------------|-------------------|------------------------------------------------------|
| **Normal**     | `< 45°C`          | Show temp on LCD only                                |
| **Warning**    | `45–65°C`         | LCD Warning + Beeping Buzzer                         |
| **Critical**   | `> 65°C`          | LCD Alert + Constant Buzzer + Red LED ON             |

---

## 🔌 Circuit Design Overview

- Thermistor connected to analog input via voltage divider  
- Buzzer and LED connected to digital outputs  
- LCD connected via 4-bit parallel mode with contrast control via potentiometer  
- Arduino processes analog values and executes logic accordingly

<img width="1241" height="687" alt="Simulation" src="https://github.com/user-attachments/assets/de1b81fe-1757-4ea4-b525-41e7f96d6f3f" />


---

## 🛠️ Tools Used

- **Arduino IDE** – Programming the microcontroller  
- **Fritzing / Proteus / Tinkercad** – (optional) Circuit simulation or design  
- **Breadboard setup** – For hardware prototyping

---

## 📋 Applications

- 🏠 **Home fire detection systems**  
- 🧪 **Lab safety and temperature monitoring**  
- 🎓 **STEM educational demonstrations**  
- 🏭 **Monitoring for temperature-sensitive equipment or rooms**

---

## 🚀 Possible Improvements

- Add **GSM module** for remote alert via SMS  
- Use **temperature logging** (SD card or serial monitor)  
- Replace thermistor with **digital sensors** like DHT22 for more accuracy  
- Integrate with **IoT platforms** for remote monitoring

---

## 📚 Conclusion

The **Fire Control System** demonstrates the powerful combination of **Arduino microcontrollers**, **sensor-based inputs**, and **real-time alerts** in creating a reliable fire warning prototype. It's simple, scalable, and serves as a great entry point for embedded systems and safety automation projects.
