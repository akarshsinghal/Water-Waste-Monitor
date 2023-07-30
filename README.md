# Water Waste Monitor

## Project Description

The Water Waste Monitor is an Arduino-based project that aims to monitor and control water usage to prevent wastage. It utilizes an ultrasonic sensor to detect the water level in a container and a sound sensor to detect the sound of running water. The project includes a Liquid Crystal Display (LCD) to provide real-time information about the water status.

## Project Setup

### Components Required

- Arduino board
- Ultrasonic sensor (HC-SR04)
- Sound sensor (e.g., KY-038)
- Liquid Crystal Display (16x2)
- Jumper wires
- Water sink

### Circuit Connection

1. Connect the ultrasonic sensor:
   - Trig pin (Sensor) to Arduino pin 13
   - Echo pin (Sensor) to Arduino pin 12

2. Connect the sound sensor:
   - DO pin (Sensor) to Arduino digital pin 7
   - AO pin (Sensor) to Arduino analog pin A0

3. Connect the Liquid Crystal Display:
   - RS pin (LCD) to Arduino pin 11
   - Enable pin (LCD) to Arduino pin 10
   - D4-D7 pins (LCD) to Arduino pins 2, 3, 4, and 5

4. Place the device beside sink for water usage to be monitored.

### Arduino Code

[Arduino Code](https://github.com/akarshsinghal/Water-Waste-Monitor/blob/main/SystemCode.cpp)

## Project Status

The Water Waste Monitor project is fully functional and can be used to monitor and control water usage. The project is complete and ready for use.

## Reflection

This project was developed by Akarsh as a personal endeavor to address the issue of water wastage. The primary goal was to build a simple monitoring system using Arduino and various sensors. Akarsh chose to use an ultrasonic sensor to measure water level and a sound sensor to detect running water. The data is displayed on an LCD screen for real-time feedback.

Challenges encountered during the development process included calibration of sensors, ensuring accurate measurements, and effectively displaying information on the LCD screen. Through research and experimentation, Akarsh was able to overcome these obstacles and create a functional water waste monitoring system.

Overall, this project served as a valuable learning experience in working with Arduino, sensors, and interfacing with an LCD display. It demonstrates Akarsh's proficiency in C++ programming for Arduino-based applications. The Water Waste Monitor is a practical and environmentally conscious project that can help users reduce water wastage and contribute to water conservation efforts.
