🚧 Mini Automated Gate System Using Arduino

An Arduino-based automated gate system that detects approaching objects, opens and closes a gate using a servo motor, and monitors object movement with an ultrasonic sensor. The system also provides real-time status updates through an I2C LCD, with LED and buzzer alerts.

📌 Project Overview

The Mini Automated Gate System demonstrates how sensors, actuators, and embedded programming can work together to automate gate operation.

An IR obstacle sensor detects an approaching object and triggers the gate to open gradually. An HC-SR04 ultrasonic sensor monitors changes in the object’s distance to help determine when the gate should close. An LCD displays the current system status, while an LED and buzzer provide additional feedback.

🎯 Project Objectives

* Automate gate opening and closing.
* Detect approaching objects using an IR sensor.
* Monitor object movement using ultrasonic distance measurements.
* Control a servo motor through programmed logic.
* Display gate status on an LCD.
* Provide visual and audible alerts.
* Practise embedded systems programming and hardware integration.
* 

🧰 Components Required
Component

Function

Arduino Uno

Main controller

IR obstacle sensor

Detects approaching objects

HC-SR04 ultrasonic sensor

Measures object distance

SG90 servo motor

Operates the gate

16×2 I2C LCD

Displays system status

LED

Visual activity indicator

Buzzer

Audible alert

Breadboard

Circuit prototyping

Jumper wires

Electrical connections

220–330 Ω resistor

Limits current through the LED

🔌 Circuit Connections
Component

Arduino Pin

IR sensor OUT

D2

LED

D4 through a resistor

Buzzer positive

D5

Servo signal

D9

HC-SR04 TRIG

D10

HC-SR04 ECHO

D11

LCD SDA

A4

LCD SCL

A5

VCC

5V, as appropriate

GND

GND
Notes:

* The LCD I2C address is 0x27.
* Connect all component grounds to a common GND.
* Connect the LED cathode to GND.
* Connect the servo’s signal wire to D9, red wire to its appropriate 5V supply, and brown/black wire to GND.
* If the servo causes resets or unstable operation, use a suitable regulated external supply with a common ground.

⚙️ How It Works

1. Standby: The gate stays closed while waiting for an object.
2. Detection: The IR sensor detects an approaching object.
3. Opening: The Arduino commands the servo to open the gate gradually.
4. Monitoring: The ultrasonic sensor measures distance as the object moves.
5. Movement analysis: The program checks changes in measured distance to help determine when the object is moving away.
6. Closing: When the programmed closing conditions are satisfied, the servo closes the gate.
7. Feedback: The LCD displays system messages, and the LED and buzzer indicate activity.

💻 Software and Libraries

* Arduino IDE
* Arduino C/C++
* Servo library
* LiquidCrystal_I2C library
* Wire library

✨ Features

* Automatic object detection
* Gradual servo-controlled gate movement
* Ultrasonic distance monitoring
* Real-time LCD status display
* LED and buzzer alerts
* Adjustable opening and closing angles
* Configurable distance thresholds

🌍 Potential Applications

* Miniature parking gate prototypes
* Model access-control systems
* Automated entry and exit demonstrations
* Robotics and embedded systems learning
* Sensor-based automation projects

This is an educational prototype, not a safety-certified gate for real vehicles or people.

🧠 Skills Demonstrated

* Embedded systems development
* Arduino programming
* Digital sensor interfacing
* Ultrasonic distance measurement
* Servo motor control
* I2C communication
* Hardware troubleshooting
* Automation and control logic

🔧 Challenges and Improvements

During testing, the gate initially took too long to close because the ultrasonic detection logic continued responding to an object that remained in the sensor’s field of view.

The program was adjusted to monitor changes in measured distance and improve the gate’s closing response.

Possible future improvements include:

* Adding a second sensor for more reliable passage detection
* Implementing obstruction detection to prevent unsafe closing
* Adding a gate-opening counter
* Introducing wireless monitoring
* Improving the gate’s mechanical design
