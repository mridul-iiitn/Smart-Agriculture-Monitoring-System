# Smart-Agriculture-Monitoring-System

This project is a Smart-Agriculture-Monitoring-System using the ESP32 microcontroller, designed to track soil moisture, temperature, and humidity, as well as detect motion using a PIR sensor. The system integrates with the Blynk IoT platform for remote monitoring and control.

# Features
Real-time Monitoring:

Soil Moisture: Measured and displayed on an LCD and Blynk.
Temperature and Humidity: Monitored using a DHT11 sensor and displayed on an LCD and Blynk.
Motion Detection: Detects motion using a PIR sensor and sends alerts via Blynk.
Control:

Relay Control: Can be controlled manually via a physical push button or remotely through Blynk.
LED Notification: Motion detection triggers an LED notification in Blynk.
User Interface:

16x2 LCD for local display of real-time data.
Blynk app for remote monitoring and control.


# Hardware Requirements
ESP32 Microcontroller
DHT11 Sensor (Temperature and Humidity)
Soil Moisture Sensor
PIR Sensor
16x2 LCD Display with I2C Module
Relay Module
Push Button
LED
Power Supply
Connecting wires and breadboard.

# Software Requirements
Arduino IDE

Install the required libraries via Arduino Library Manager:
BlynkSimpleEsp32
LiquidCrystal_I2C
DHT
Blynk IoT Platform

Create a project in the Blynk app.
Add widgets for:
Virtual Pins:
V0 - Temperature
V1 - Humidity
V3 - Soil Moisture
V5 - PIR Motion LED
V12 - Relay Control
Event Notification: For motion detection alerts.
# Circuit Diagram
Soil Moisture Sensor: Connect to GPIO 0 (analog read).
PIR Sensor: Connect to GPIO 14.
Relay Module: Connect to GPIO 5.
Push Button: Connect to GPIO 25 with an internal pull-up resistor.
DHT11 Sensor: Data pin connected to GPIO 32.
LCD Display: SDA and SCL connected to the appropriate I2C pins.
# How to Run the Project
Setup Blynk:

Get your Blynk template ID, name, and authentication token.
Replace the placeholders in the code with your credentials.
Configure WiFi:

Replace the ssid and pass variables with your WiFi credentials.
Upload the Code:

Compile and upload the code to the ESP32 using the Arduino IDE.
Monitor and Control:

Open the Blynk app to monitor the sensor data and control the relay.
View real-time data on the LCD display.
# Code Highlights
DHT11 Sensor:
Measures temperature and humidity and sends data to Blynk (V0 and V1).
Soil Moisture Sensor:
Reads analog soil moisture values and maps them to percentages (V3).
PIR Sensor:
Detects motion and sends a notification via Blynk (V5).
Relay Control:
Physical button toggles relay state.
Remote control via Blynk on V12.
# Improvements and Future Work
Add an automatic irrigation system based on soil moisture levels.
Enhance power efficiency for prolonged operation.
# Contributing
Feel free to fork the repository and contribute to enhancing this project. Submit a pull request with your changes for review.
