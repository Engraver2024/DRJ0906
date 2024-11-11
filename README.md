the manueal  
User Manual for Smart Enclosure V5
1. Overview
The Smart Enclosure V5 is designed to provide optimal environmental control with real-time monitoring and automated venting based on temperature and gas levels. This system includes enhanced sensors for accurate temperature and humidity measurement, automated servo vent control, and real-time tracking with an RTC module. New features in V5 include upgrading from the DHT11 sensor to a DHT22 for better accuracy, adding a servo motor for automatic and manual venting, and introducing a five-button interface for versatile control options.

2. Components and Setup
Required Components
Arduino Uno
DHT22 Temperature and Humidity Sensor: Measures temperature and humidity more accurately than the previous DHT11.
MQ2 Gas Sensor: Monitors gas and pollutant levels.
Servo Motor (9g): Controls the vent door based on environmental data.
DS1302 Real-Time Clock (RTC) Module: Keeps time for scheduling; requires periodic calibration.
Buzzer: Alerts users when thresholds are exceeded.
LCD Display (20x4): Shows real-time data and alerts.
Push Buttons (5): For user control.
Breadboard, jumper wires, and resistors (as necessary for button connections).
Assembly Instructions
Sensor Connections:

Connect the DHT22 sensor to a digital pin on the Arduino (data, power, and ground).
Connect the MQ2 sensor to the Arduino with similar connections.
Servo Motor Setup:

Connect the servo motor to PWM-capable pin (e.g., pin 11) for control.
RTC Module Setup:

Connect the DS1302 using its data, clock, and power pins.
Ensure the RTC battery is functional for uninterrupted timekeeping.
Button Wiring:

Connect each button to a digital input pin on the Arduino, using pull-down resistors or the Arduino's internal pull-ups.
Buzzer and LCD:

Connect the buzzer to a designated digital pin.
Wire the LCD to the Arduino following the 20x4 display configuration guide.
3. Button Functions and Operations
Each button has a specific function for system control:

Button 1: Adjusts temperature thresholds for triggering the servo motor.
Button 2: Mutes/unmutes the buzzer to silence alarms when needed.
Button 3: Toggles between automatic and manual control of the servo motor.
Button 4: Resets the system, recalibrating sensors as necessary.
Button 5: Manually opens/closes the servo vent, overriding automatic control temporarily.
4. Operating the System
Power On: Connect the Arduino to power to initialize the system.
Data Display: The LCD shows real-time temperature, humidity, gas levels, and system alerts.
Automatic Vent Control: The servo motor will adjust the vent position based on temperature or gas thresholds unless manual control is activated.
Manual Control: Use Button 5 for manual servo operation; Button 3 to switch between automatic and manual modes.
5. Maintenance
RTC Calibration and Battery Replacement
Calibration: Regularly update the DS1302 clock for accurate timekeeping.
Battery: Replace the RTC module battery as needed to ensure continuous operation.
Sensor Calibration
DHT22 and MQ2 Calibration: Calibrate these sensors periodically according to manufacturer recommendations to maintain accuracy.
Button and Servo Maintenance
Buttons: Ensure they respond to presses; replace any worn-out buttons.
Servo Motor: Check for smooth operation and keep it clean from dust or debris.
6. Troubleshooting
Common Issues and Fixes
Servo Not Moving:

Check wiring and power supply.
Ensure the correct pin is used in the code.
Inaccurate Readings:

Recalibrate the DHT22 and MQ2 sensors.
Verify sensor connections.
Buzzer Won't Silence:

Ensure Button 2 is functioning.
Check the mute logic in the code.
}
7. Update Log (Version 5)
Upgraded Sensor: DHT11 has been replaced with DHT22 for improved temperature/humidity accuracy.
Servo Motor Integration: Servo is added for vent control based on sensor readings.
RTC Module Calibration: DS1302 requires regular updates for accuracy.
Five Buttons Added: Expanded user control with added button functions.
