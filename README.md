# Smart Healthcare Patient Health Monitoring and Emergency Assistance System using LPC2129

An IoT-based Smart Healthcare System developed using the **LPC2129 (ARM7)** microcontroller. The system continuously monitors vital health parameters such as **Heart Rate**, **Blood Oxygen Saturation (SpO₂)**, **Body Temperature**, and **Distance**, displays the readings on a **16×2 LCD**, and transmits the collected data through Wi-Fi for remote monitoring. The system also provides visual and audible alerts whenever abnormal conditions are detected.

---

## Features

- Real-time Heart Rate Monitoring
- Blood Oxygen Saturation (SpO₂) Measurement using MAX30102
- Body Temperature Monitoring using DHT11
- Distance Measurement using HC-SR04 Ultrasonic Sensor
- LCD Display for Local Monitoring
- UART Communication for Debugging and IoT Communication
- Wi-Fi Connectivity using ESP8266
- LED and Buzzer Alerts for Emergency Conditions
- Modular Driver-Based Embedded Software Architecture

---

## Hardware Components

- LPC2129 (ARM7) Microcontroller
- MAX30102 Pulse Oximeter Sensor
- DHT11 Temperature Sensor
- HC-SR04 Ultrasonic Sensor
- ESP8266 Wi-Fi Module
- 16×2 LCD Display
- Buzzer
- LED Indicator
- LPC2129 Development Board

---

## Software & Tools

- Embedded C
- Keil uVision IDE
- LPC2129 ARM7 Microcontroller
- UART Communication
- I2C Communication
- GPIO Programming
- Timer Programming
- Interrupt Handling

---

# Repository Structure

```
Smart_Healthcare_Monitoring/
│
├── main.c              # Main application logic
├── header.h            # Function declarations, macros and definitions
├── delay.c             # Delay routines
├── uart0_driver.c      # UART0 driver implementation
├── i2c_driver.c        # I2C driver implementation
├── lcd_driver.c        # LCD driver
├── dth11.c             # DHT11 temperature sensor driver
├── ultra.c             # HC-SR04 ultrasonic sensor driver
├── iot.c               # ESP8266 Wi-Fi communication
├── heart.c             # Heart rate calculation
├── spo2.c              # SpO₂ calculation
├── interrupt.c         # Interrupt service routines
├── handler.c           # Exception handlers
└── README.md
```

---

# Getting Started

## Clone the Repository

Clone the project using Git.

```bash
git clone https://github.com/<your-github-username>/Smart_Healthcare_Monitoring.git
```

Move into the project directory.

```bash
cd Smart_Healthcare_Monitoring
```

---

# Import the Project into Keil uVision

1. Open **Keil uVision**.
2. Create a **New Project** or open your existing LPC2129 project.
3. Select the target device:
   - **NXP → LPC2129**
4. Right-click **Source Group 1**.
5. Select **Add Existing Files to Group 'Source Group 1'**.
6. Add the following source files:

```
main.c
delay.c
uart0_driver.c
i2c_driver.c
lcd_driver.c
dth11.c
ultra.c
iot.c
heart.c
spo2.c
interrupt.c
handler.c
```

7. Add the header file:

```
header.h
```

8. Configure the target settings if required.
9. Save the project.

---

# Build the Project

Build the project using:

```
Project → Build Target
```

or simply press:

```
F7
```

Ensure there are no compilation errors.

---

# Download to LPC2129

1. Connect the LPC2129 development board.
2. Flash the generated HEX file using Flash Magic or your preferred programming tool.
3. Reset the board after programming.

---

# Functional Overview

The application performs the following tasks:

1. Initializes UART, GPIO, Timers, LCD and I2C peripherals.
2. Reads body temperature using the DHT11 sensor.
3. Collects Red and IR samples from the MAX30102 sensor.
4. Calculates Heart Rate and SpO₂.
5. Measures distance using the HC-SR04 ultrasonic sensor.
6. Displays sensor readings on the LCD.
7. Sends sensor data to the IoT platform using the ESP8266 Wi-Fi module.
8. Activates the LED and Buzzer whenever abnormal conditions are detected.

---

# Communication Interfaces

- UART
- I2C
- GPIO
- Timers
- External Interrupts

---

# Concepts Demonstrated

- Embedded C Programming
- ARM7 LPC2129
- Device Driver Development
- UART Communication
- I2C Communication
- GPIO Programming
- Timer Programming
- Interrupt Handling
- Sensor Interfacing
- Embedded Signal Processing
- Real-Time Embedded Systems
- IoT Integration
- Modular Embedded Software Design

---

# Future Improvements

- ECG Sensor Integration
- Cloud Database Storage
- Mobile Application
- MQTT Communication
- SMS/Email Alerts
- Patient History Logging
- Battery Health Monitoring

---

# Contributors

- **Keshav Babu** (@keshavbabu0112)
- **Vikas Stalin** (@stalinmade)
- **Tanmaye M S** (@mstanmaye)

