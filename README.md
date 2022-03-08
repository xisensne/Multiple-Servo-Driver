# Multiple-Servo-Driver

An ArduinoProgram to drive up to 6 servos on an Arduino Nano/Uno

This program allows control of up to six low cost servo motors which may be sed for controlling model railway turnouts, signals or accessories using a small arduino processor.  It was originnaly intended for an arduino Nano.

The program allows setting end points for the movement of the servos using a number of pushbuttons.  These values are stored in the EEPROM of the microprocessor.

The servos are operated by switches attached to the relevant input pins.  The programming is carried out by buttons attached to the programming pins.

**Please Note:**
The servo control pins are attached to the Nano pins, but the servos should be powered by an indepedent 5V power supply.  Attempting to drive the servos from the Nano 5V pin would undoubtedly destroy the Nano.

## Pin Configurations

**Servo Pins**
- Servo 1 to pin 8
- Servo 2 to pin 9
- Servo 3 to pin 10
- Servo 4 to pin 11
- Servo 5 to pin 12
- servo 6 to pin 3

**Lever Pins**
The operating levers/switches connect to pins 14 to 19 in order of the servos

**Programming Buttons**
Four buttons can be connected temporarily to the following four pins in order to set the servo end points:
- Low Button - Pin 7
- Prog Button - Pin 6
- High Button - Pin 5
- Mode Button - Pin 4

## Programming Method
1. To put the unit into program mode press the **PROG** button.  This will set the Nano into program mode on Servo Channel 1.  The Nano will flash the internal LED once to indicate channel.
The servo will be centralised.
2. To move the servo arm to the low position press the **LOW** button. If you hold the button down the arm will keep moving.
3. To move the servo arm to the high position press the **HIGH** button.
4. If you wish to reverse the Low and High postions press gthe **Mode** button once.
5. Once you are happy with the settings press the **Mode** button again.  This will move up to the next Servo channel and the onboard LED will start flashing at a different rate (i.e. 2 flashes for channel 2 and so on).
6. Once you have reached the last channel the servos will move to the low positions, the LED will stop flashing and the setting will be saved to EEPROM
7. Operating a Lever/Switch should now operate the servo.


## Source Files

This repository contains three source files.
- ServoDriverMultiv4.ino.  This is the main source file for the code which will control six servos.#
- ServoDriverMultiTwoServos.ino.  This file has been configured to operate two servos.
- ServoDriverMultiFourServos.ino.  This file has been configured to operate four servos.

The code uses three libraries which will need to be loaded into the Arduino IDE
1. EEPROM - This is part of the Arduino infrasructure.
2. Button - 
3. VarSpeedServo -

