# Practical-1---DAIOT
Introduction to Arduino and Raspberry Pi.
# Aim-- To Study the Arduino and Raspberry Pi.
# Theory
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
#Materials Required
~ Arduino Uno board

~Raspberry Pi (any model)
~ USB cable for Arduino
~ Breadboard
~Jumper wires
~ LED


~ 220-ohm resistor
~ DHT11 Temperature and Humidity Sensor
~ MicroSD card with Raspbian OS (for Raspberry Pi)
~ Monitor, keyboard, and mouse (for Raspberry Pi)
~
# Procedure
Part 1: Arduino Setup
1. Connect the LED:
o Place the LED on the breadboard.
o Connect the anode (long leg) of the LED to digital pin 9 on the Arduino through a
220-ohm resistor.
o Connect the cathode (short leg) to the ground (GND) on the Arduino.
2. Upload the Arduino Sketch:
o Open the Arduino IDE on your computer.
o Write and upload the following code to the Arduino:


Part 2: Raspberry Pi Setup
~ Insert the microSD card into the Raspberry Pi.
~Connect the monitor, keyboard, and mouse.
~ Power up the Raspberry Pi and complete the initial setup.
~. Install Python Serial Library:
~ Open a terminal window on the Raspberry Pi.
~ Install the pyserial library with:
bash

Fig:-Arduino board connected to the LED

# Working
Arduino Operation:
The Arduino code continuously toggles the LED on and off every second while sending serial
messages (&quot;LED ON&quot; and &quot;LED OFF&quot;) to the connected serial port.
Raspberry Pi Operation:
The Python script running on the Raspberry Pi reads the serial messages sent by the Arduino and
prints them to the terminal. This allows the Raspberry Pi to monitor the status of the LED on the
Arduino.


1 arduino:-
In the year 2005, the classrooms of
the Interactive Design Institute in
Ivrea, Italy, first introduced the
Arduino board.
1. rasberry:-
In the year 2012, Eben Upton first
introduced the Raspberry Pi device in
February.
2. arduino
 Control unit of the Arduino is from
the Atmega family.
2. rasberry
The control unit of Raspberry Pi is from the
ARM family.
3 .arduino
 Arduino is based on a microcontroller.
3.rasberry
While Raspberry Pi is based on a
microprocessor.
4.arduino
It is designed to control the electrical
components connected to the circuit
board in a system.
4. rasberry
While Raspberry Pi computes data and
produces valuable outputs, and controls
components in a system based on the
outcome of its computation.
5.arduino
 Arduino boards have a simple
hardware and software structure.
5.rasberry
While Raspberry Pi boards have a complex
architecture of hardware and software.

6. arduino
CPU architecture: 8 bit.
6 rasberry
 CPU architecture: 64 bit.

7.arduino
It uses very little RAM, 2 kB.
7.rasberry
While Raspberry Pi requires more RAM, 1

8.arduino
 It clocks a processing speed of 16
MHz.
8. rasberry
While Raspberry Pi clocks a processing
speed of 1.4 GHz.

9 arduino
It is cheaper in cost.
9.rasberry
While Raspberry Pi is expensive.
10. arduino
 It has a higher I/O current drive
strength.
10 . rasberry
While Raspberry Pi has a lower I/O current
drive strength.
11 arduino
It consumes about 200 MW of power.
11 rasberry
While it consumes about 700 MW of power.
12. arduino
 Its logic level is 5V. 
 12. rasberry
 Its logic level is 3V.
 13 arduino
 It does not have internet support
 13. rasberry
 It has inbuilt Ethernet port and WiFi
support.

14.arduino
It has higher current drive strength.
14.rasberry
It has lower current drive strength.
15 arduino
Some of the applications of Arduino
are traffic light countdown timer ,
Weighing machines , etc.
15 rasberry
Some of the applications of Raspberry Pi are
Stop motion cameras , Robot Controllers ,
Game Servers.
16 arduino
 Operating systems are required in
Arduino.
16 rasberry
Operating System is required in Raspberry
Pi.

# Conclusion
The lab exercise successfully demonstrated the basic operations of Arduino and Raspberry Pi, as
well as how to establish serial communication between them. By completing this experiment,
students gained practical experience in interfacing microcontrollers with single-board computers
and understood the fundamentals of serial data exchange.
