This repo was made for the event `FabLab Hands-on Open House - Arduino Edition`, for new students of 42 Berlin to get to the know the FabLab and especially the 'clean lab'. Over the course of a few hours, we will build a project together which involves some fabrication (3D printing, laser cutting, soldering, glue/paper/scissors). As part of the process we will get know:

- the different types of Arduino, components and sensors we have the lab and how to use them
- how to upload code to an Arduino using the Arduino IDE 
- how to simulate Arduino-based circuits and code using Tinkercad
- how to use a breadboard
- ...and much more

# Prerequisites

Make an account on [Tinkercad](https://www.tinkercad.com/)

# Getting Started

[Getting Started Guide](GettingStarted.md)

# The Project(s)

1. [Arduino Maze Robot](https://www.tinkercad.com/projects/Simple-Arduino-Maze-Robot-for-Project-Based-Learni)

- 2x SG90 micro servos w/ servo arms and screws
- KY023 joystick
- 13x Metric M2 x 8 mm Phillips flat head self tapping screws (link removed) (avoid the black screws, they break and strip easily)
- 2x 1/8 x 5/16 rivets (just the head)
- 2x - 4-40 x 1/2" machine screw 
- 2x - 4-40 machine screw nut

2. [Rock-Paper-Scissors Robot](https://www.tinkercad.com/projects/Rock-Paper-Scissors-Using-Tinkercad-Circuits-and-A)

- use larger servos, we need the mini's for another project
- demo this project, as we have it built already

3. [Sun Tracking Sunflower Robot](https://www.tinkercad.com/projects/How-to-Make-Sun-Tracking-Sunflower-Robot-Using-Ard)

Key part:
- Micro servo

# Starter Projects

Start here to practice with individual components
- each project has contains a Tinkercad "Preview" - a simulation of the project
- simulate it first in Tinkercad, then try to make it with a real Arduino

Motors: 
Sensing
	- LDRs
	- Distance sensor: https://www.tinkercad.com/projects/Ultrasonic-Distance-Sensor-Arduino-Tinkercad
Light
	- LEDs
Sound
	- Buzzer: https://www.tinkercad.com/things/81sIEGzvYqU-super-mario-theme

# Arduino Quickstart Guide (for the boards we have)

- [Download](https://www.arduino.cc/en/software) and install the newer version 2 IDE, there are many improvements over the v1. This should be installed on all FabLab PC's.

Using the [Arduino Web Editor](https://docs.arduino.cc/learn/starting-guide/the-arduino-web-editor/) is also a possibility in order to use your Arduino directly from the browser, but requires an account and install of the Arduino Create Agent.

## Arduino Uno

- Choose `Tools -> Boards -> Arduino AVR Boards -> Arduino Uno`
- First look in `Tools -> Ports` to see which items are already there
- Now connect it (I used one of the short blue USB cables)
- Then in `Tools -> Ports` select the item that appeared (in newer ArduinoIDE the item is also named after the board)
- Open the onboard LED Blink example from `File -> Examples -> 01.Basics -> Blink`
- If the blink example is already loaded on the board, modify the code slightly to change blink range i.e. `delay(100)` instead of `delay(1000)`
- Click the upload (`->`) button, code should flash, `Done Uploading` message should appear and onboard LED should blink

## Arduino Uno Wifi (Rev 2)

https://docs.arduino.cc/retired/getting-started-guides/ArduinoUnoWiFi/

Do not be tempted to select `Arduino Uno Wifi` in the boards list, this is for the older revision of the board! If you try you will get the classic error:
```
avrdude: stk500_recv(): programmer is not responding
avrdude: stk500_getsync() attempt 1 of 10: not in sync: resp=0x00
```

Instead:
- In `Tools -> Boards -> Board Manager` search `Arduino megaAVR Boards` and click install
- Then choose `Tools -> Boards -> Arduino megaAVR Boards -> Arduino Uno Wifi Rev2`
- First look in `Tools -> Ports` to see which items are already there
- Now connect the Arduino to your PC (I used one of the short blue USB cables)
- Then in `Tools -> Ports` select the item that appeared (in newer ArduinoIDE the item is also named after the board)
- Open the onboard LED Blink example from `File -> Examples -> 01.Basics -> Blink`
- If the blink example is already loaded on the board, modify the code slightly to change blink range i.e. `delay(100)` instead of `delay(1000)`
- Click the upload (`->`) button, code should flash, `Done Uploading` message should appear and onboard LED should blink

Note, I get the warning
`avrdude: usbdev_open(): WARNING: failed to set configuration 1: Device or resource busy`

## Arduino MKR Wifi 1010

Follow [this tutorial](https://www.arduino.cc/en/Guide/MKRWiFi1010) or in brief:
- In `Tools -> Boards -> Board Manager` choose `Arduino SAMD Boards (32-bits ARM Cortex-M0+)` and wait for install
- No wifi driver installation is necessary for Linux
- First look in `Tools -> Ports` to see which items are already there
- Then connect the Arduino with a microUSB cable 
- Then in `Tools -> Ports` select the item that appeared (in newer ArduinoIDE the item is also named after the board)
- If no extra entry appears, it could be a cable issue (I switched to another)
- Open the onboard LED Blink example from `File -> Examples -> 01.Basics -> Blink`
- Code should flash and onboard LED should start blinking. Successful upload message looks like this: 

```
Write 12312 bytes to flash (193 pages)

[=========                     ] 33% (64/193 pages)
[===================           ] 66% (128/193 pages)
[============================= ] 99% (192/193 pages)
[==============================] 100% (193/193 pages)
done in 0.080 seconds

Verify 12312 bytes of flash with checksum.
Verify successful
done in 0.011 seconds
CPU reset.
```

## Arduino Nano (To Add)

- select old bootloader