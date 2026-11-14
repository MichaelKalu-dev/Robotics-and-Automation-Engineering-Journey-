Project 03: Smart Parking Barrier 🚗

Overview

An Arduino-based smart parking barrier that uses an ultrasonic sensor to detect approaching objects. When an object is detected within 20 cm, a servo motor raises the barrier and the green LED turns on. When the object moves beyond the threshold, the barrier closes and the red LED turns on.

This project demonstrates basic sensor integration, distance measurement, conditional logic, LED indicators, and servo motor control.

Objectives

- Detect nearby objects using an HC-SR04 ultrasonic sensor.
- Measure distance and compare it against a defined threshold.
- Automatically open and close a barrier using a servo motor.
- Use red and green LEDs to indicate the barrier's status.
- Integrate multiple electronic components into one Arduino system.

Components Used

- Arduino Uno
- HC-SR04 ultrasonic distance sensor
- Micro servo motor
- Red LED
- Green LED
- 2 resistors for the LEDs
- Breadboard
- Jumper wires

Pin Connections

Component| Arduino Pin
Ultrasonic TRIG| D13
Ultrasonic ECHO| D12
Green LED| D5
Red LED| D10
Servo signal| D3

The ultrasonic sensor and servo also require appropriate power and ground connections.

How It Works

1. The Arduino sends a trigger pulse to the ultrasonic sensor.
2. The sensor returns an echo pulse corresponding to the measured distance.
3. The Arduino calculates the approximate distance in centimetres.
4. If the distance is 20 cm or less, the servo moves to 90°, the green LED turns on, and the red LED turns off.
5. If the distance is greater than 20 cm, the servo moves to 0°, the red LED turns on, and the green LED turns off.

Circuit Simulation

"Smart Parking Barrier circuit simulation" (circuit.jpg)

Project Concept

"Smart Parking Barrier concept" (Project.png)

The concept image illustrates the intended system. The circuit screenshot shows the actual simulation.

Testing and Results

Test| Expected behaviour| Result
No object within the detection threshold| Barrier closes; red LED turns on| Passed
Object detected within 20 cm| Barrier opens; green LED turns on| Passed
Object moves away| Barrier closes; red LED turns on| Passed
Object moves around the threshold| System responds to distance changes| Passed
No echo / sensor failure| Safe and predictable response| Not tested

Known Limitations

- The system has not yet been tested for ultrasonic sensor failure or missing echo readings.
- The current implementation does not include filtering or hysteresis to prevent rapid switching when measurements fluctuate near the threshold.
- The prototype has been tested in Tinkercad simulation; physical hardware testing remains necessary.

Skills Demonstrated

- Arduino programming with C/C++
- Ultrasonic distance measurement
- Digital input/output
- Conditional logic
- Servo motor control
- Electronic circuit assembly and simulation
- System integration and functional testing

Tools

- Arduino IDE-compatible programming
- Tinkercad Circuits
- GitHub

Future Improvements

- Handle missing or invalid sensor readings safely.
- Add hysteresis or filtering for more stable operation.
- Improve barrier movement and vehicle detection reliability.
- Test the system using physical hardware.

---

Project status: Core functionality implemented and tested in simulation.
