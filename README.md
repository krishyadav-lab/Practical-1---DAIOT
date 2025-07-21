# Practical-1---DAIOT
Introduction to Arduino and Raspberry Pi.
1. Aim-- To Study the Arduino and Raspberry Pi.
2. Theory
Arduino
Arduino is an open-source electronics platform that provides a simple microcontroller-based
environment for creating interactive electronic projects. It uses a straightforward programming
language and IDE to control digital and analog components.
Raspberry Pi
Raspberry Pi is a compact, versatile computer that runs a full operating system and can interface
with external hardware through its GPIO pins. It supports various programming languages,
including Python, which is often used for controlling hardware.

Serial Communication
Serial communication is a method for transmitting data between devices. Arduino and Raspberry
Pi can communicate via serial ports, allowing data to be sent and received. This is useful for
integrating sensor data or control signals between the two platforms.
3. Materials Required
 Arduino Uno board
 Raspberry Pi (any model)
 USB cable for Arduino
 Breadboard
 Jumper wires
 LED

Lab Manual IOT &amp; DA

7 | Page

 220-ohm resistor
 DHT11 Temperature and Humidity Sensor
 MicroSD card with Raspbian OS (for Raspberry Pi)
 Monitor, keyboard, and mouse (for Raspberry Pi)

4. Procedure
Part 1: Arduino Setup
1. Connect the LED:
o Place the LED on the breadboard.
o Connect the anode (long leg) of the LED to digital pin 9 on the Arduino through a
220-ohm resistor.
o Connect the cathode (short leg) to the ground (GND) on the Arduino.
2. Upload the Arduino Sketch:
o Open the Arduino IDE on your computer.
o Write and upload the following code to the Arduino:
cpp
Copy code
void setup() {
Serial.begin(9600); // Initialize serial communication
pinMode(9, OUTPUT); // Set pin 9 as output
}
void loop() {
digitalWrite(9, HIGH); // Turn the LED on
Serial.println(&quot;LED ON&quot;);
delay(1000); // Wait for a second
digitalWrite(9, LOW); // Turn the LED off
Serial.println(&quot;LED OFF&quot;);
delay(1000); // Wait for a second
}

Part 2: Raspberry Pi Setup
1. Prepare Raspberry Pi:
o Insert the microSD card into the Raspberry Pi.
o Connect the monitor, keyboard, and mouse.
o Power up the Raspberry Pi and complete the initial setup.
2. Install Python Serial Library:
o Open a terminal window on the Raspberry Pi.
o Install the pyserial library with:
bash

Lab Manual IOT &amp; DA

8 | Page

Copy code
sudo apt-get update
sudo apt-get install python3-serial

3. Create Python Script:
o Create a Python script to read the serial data from Arduino. Open a text editor and
write the following script:
python
Copy code
import serial
# Open serial port
ser = serial.Serial(&#39;/dev/ttyACM0&#39;, 9600)
while True:
try:
line = ser.readline().decode(&#39;utf-8&#39;).strip()
print(line)
except KeyboardInterrupt:
break
ser.close()
4. Run the Script:
o Save the Python script as read_serial.py.
o Execute the script by running:
bash
Copy code
python3 read_serial.py
5. Connect Arduino to Raspberry Pi:
o Connect the Arduino to the Raspberry Pi using a USB cable.

5. Image

Lab Manual IOT &amp; DA

9 | Page

Fig:-Arduino board connected to the LED

6. Working
Arduino Operation:
The Arduino code continuously toggles the LED on and off every second while sending serial
messages (&quot;LED ON&quot; and &quot;LED OFF&quot;) to the connected serial port.
Raspberry Pi Operation:
The Python script running on the Raspberry Pi reads the serial messages sent by the Arduino and
prints them to the terminal. This allows the Raspberry Pi to monitor the status of the LED on the
Arduino.

S
No.
Arduino Raspberry Pi

1.
In the year 2005, the classrooms of
the Interactive Design Institute in
Ivrea, Italy, first introduced the
Arduino board.

In the year 2012, Eben Upton first
introduced the Raspberry Pi device in
February.

2. Control unit of the Arduino is from
the Atmega family.

The control unit of Raspberry Pi is from the
ARM family.

3. Arduino is based on a microcontroller. While Raspberry Pi is based on a

microprocessor.

4.
It is designed to control the electrical
components connected to the circuit
board in a system.

While Raspberry Pi computes data and
produces valuable outputs, and controls
components in a system based on the
outcome of its computation.

5. Arduino boards have a simple
hardware and software structure.

While Raspberry Pi boards have a complex
architecture of hardware and software.

Lab Manual IOT &amp; DA

10 | Page

6. CPU architecture: 8 bit. CPU architecture: 64 bit.

7. It uses very little RAM, 2 kB. While Raspberry Pi requires more RAM, 1

GB.
8. It clocks a processing speed of 16
MHz.

While Raspberry Pi clocks a processing
speed of 1.4 GHz.

9. It is cheaper in cost. While Raspberry Pi is expensive.
10. It has a higher I/O current drive
strength.

While Raspberry Pi has a lower I/O current
drive strength.

11. It consumes about 200 MW of power. While it consumes about 700 MW of power.
12. Its logic level is 5V. Its logic level is 3V.
13. It does not have internet support. It has inbuilt Ethernet port and WiFi

support.

14. It has higher current drive strength. It has lower current drive strength.

15.
Some of the applications of Arduino
are traffic light countdown timer ,
Weighing machines , etc.

Some of the applications of Raspberry Pi are
Stop motion cameras , Robot Controllers ,
Game Servers.

16. Operating systems are required in
Arduino.

Operating System is required in Raspberry
Pi.

7. Conclusion
The lab exercise successfully demonstrated the basic operations of Arduino and Raspberry Pi, as
well as how to establish serial communication between them. By completing this experiment,
students gained practical experience in interfacing microcontrollers with single-board computers
and understood the fundamentals of serial data exchange.
