Welcome to the `FabLab Hands-on Open House - Arduino Edition` :wave:

This event is for new students of 42 Berlin to get to the know the FabLab and especially the 'clean lab'.

Over the course of the next few hours, we will build an Arduino project together which involves electronics, code and some fabrication (3D printing, laser cutting, soldering, glue/paper/scissors).

As part of the process we will get know:
- the different types of Arduino, components and sensors we have the lab and how to use them
- how to upload code to an Arduino using the Arduino IDE
- how to simulate Arduino-based circuits and code using Tinkercad
- how to use a breadboard
- ...and much more!

If you enjoy this session, watch out for the upcoming Microcontroller Makerthon taking place over a weekend in the lab!

# Prerequisites

- Make an account on [Tinkercad](https://www.tinkercad.com/). Tinkercad is an intuitive online platform for designing 3D models and circuit design. We will simulate all circuits in Tinkercad first before building them in real life.
- [Download](https://www.arduino.cc/en/software) and version 2 of the Arduino IDE. There are many improvements over the v1! This should already be installed on all FabLab PC's.

# The Projects

There are three projects to choose from, to work on in teams. I will introduce all of them here so you can see the 'end goal', but it's recommended to
- start small with the [Tutorials and examples](#tutorials-and-examples) section below
- simulate the project first in Tinkercad as far as you can before trying to build it with a real Arduino (each project should contains a Tinkercad "Preview")

1. [Arduino Maze Robot](https://www.tinkercad.com/projects/Simple-Arduino-Maze-Robot-for-Project-Based-Learni)

Key components:
- 2x SG90 micro servos w/ servo arms and screws
- KY023 joystick
- 13x Metric M2 x 8 mm Phillips flat head self tapping screws (avoid the black screws, they break and strip easily)
- 2x 1/8 x 5/16 rivets (just the head)
- 2x 4-40 x 1/2" machine screw 
- 2x 4-40 machine screw nut

2. [Rock-Paper-Scissors Robot](https://www.tinkercad.com/projects/Rock-Paper-Scissors-Using-Tinkercad-Circuits-and-A)

Key components:
- larger servos (we need the mini ones for another project)

3. [Sun Tracking Sunflower Robot](https://www.tinkercad.com/projects/How-to-Make-Sun-Tracking-Sunflower-Robot-Using-Ard)

Key components:
- one micro servo e.g. SG90

# Tutorials and examples

Start here to practice on a smaller scale with the Arduino and individual components, before 'scaling up' to build your full team project

## Some basics 
- Introducing the Breadboard(https://www.tinkercad.com/learn/overview/OPRHCXXL20FZS3N?collectionId=O0K87SQL1W5N4P2&type=circuits)
- Wiring Components(https://www.tinkercad.com/learn/overview/OLORCO6L20FZRZ7?collectionId=O0K87SQL1W5N4P2&type=circuits)
- Start Simulating(https://www.tinkercad.com/learn/overview/OT2JZ1PL20FZRMO?collectionId=O0K87SQL1W5N4P2&type=circuits)
- Using the Serial Monitor(https://www.tinkercad.com/learn/overview/OZ3W85UL26F9GZH?collectionId=O0K87SQL1W5N4P2&type=circuits)

## Learning about key components
Light
	- [Fading LED With Analog Output](https://tinkercad.com/learn/overview/ORHT6NFL26F9GSW?collectionId=O0K87SQL1W5N4P2&type=circuits)
Sensing
	- [Light Dependent Resistors](https://www.tinkercad.com/learn/overview/OXQL7IEL26F9H0U?type=circuits)
	- [Distance sensor](https://www.tinkercad.com/projects/Ultrasonic-Distance-Sensor-Arduino-Tinkercad)
Motors:
	- [Using Servos](https://www.tinkercad.com/things/eqQfhbhZPNa-arduino-uno-tutorial-3-servo-motor-project)
	- be aware that there are different types of servos e.g
	 	- standard servos which have a limited range of motion
		- continuous rotation servos which can rotate continuously in either direction
Sound_
	- [Super-Mario Buzzer](https://www.tinkercad.com/things/81sIEGzvYqU-super-mario-theme)

# Arduino Quickstart Guide (for the boards we have)

One of the hardest parts of Arduino is setting up your board so you can upload code to it. This process is still not quite 'plug and play'. I have provided a concice guide here for each of the flavours of Arduino we have in the lab.

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

- Note: select old bootloader!!