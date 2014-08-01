tinyISPShield
=============

** Important **
This project is in development and presently untested. Operation is
described as intended. This may not work at all, or worse, may damage your
parts or equipment. All risks are yours alone.

An Arduino UNO R3 Shield for programming ATtiny44/45/84/85 MCUs with Arduino 
sketches.

Arduino 1.0.5 comes with an example sketch named ArduinoISP. That sketch 
turns an Arduino Uno into a sketch programmer for other Atmel MCUs.

For more info on programming ATtiny series MCUs with Arduino sketches see 
[High-low tech blog](http://highlowtech.org/?p=1695)

Eagle CAD 6.5 Hobbist Edition used. Latest PCB available from 
[OSHPark](https://oshpark.com/shared_projects/PF0k6TW9)

Usage
-----

Choose the correct locations for the 3 MCU type selection jumper shunts.
They should all be aligned and all are necessary. Choose either:

- ATtiny44/84 (14-pin PDIP) or 
- ATtiny45/85 (8-pin PDIP).

Connect the shield to an Arduino UNO R3 and connect the Arduino to your
computer with a USB cable. The green READY LED should be blinking. If it
is not, check the connection and/or ensure the ArduinoISP sketch is loaded
on the base Arduino and that it is powered correctly.

1-Open the Arduino 1.0.5 IDE and load the sketch you want to upload to your
ATtiny part.
2-Choose the correct MCU from the IDE's Tools > Boards menu,
3-Choose 'Arduino as ISP' from the Tools > Programmer menu.
4-Insert the target ATtiny MCU in the ZIF socket. Verify the correct location
for pin 1 and the type selection jumper shunts.
5-Upload the sketch.

The yellow BUSY LED will illuminate when the part is being programmed.

The red ERROR LED will illuminate if there was an error uploading the 
last sketch.

Building
--------

I encourage you to build your own if you want to or find yourself using
ATtiny's for many projects. The ZIF if a 14 pin 3M "textool" 214-3339 part
available from Digikey. It's under $20. Not the cheapest. It does however
have 30um gold flash, 3x that of comparable parts in the Digikey catalog.
I personally hate tools that suck so I opted for the better part, I only
need one. Rework it as you please.

The LEDs and limiting resistors are all optional. You can get away with
as few parts as the PCB, ZIF, a 2 pin and 4 pin 0.100" header. I populated
2 pins on each corner of the Arduino header layout for stability and ease
of alignment.

Development
-----------

If you wish to develop this project further please fork it on github.


