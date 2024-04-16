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

## Arduino Uno Wifi

https://docs.arduino.cc/retired/getting-started-guides/ArduinoUnoWiFi/

Sketch uses 932 bytes (2%) of program storage space. Maximum is 32256 bytes.
Global variables use 9 bytes (0%) of dynamic memory, leaving 2039 bytes for local variables. Maximum is 2048 bytes.
avrdude: stk500_recv(): programmer is not responding
avrdude: stk500_getsync() attempt 1 of 10: not in sync: resp=0x00

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