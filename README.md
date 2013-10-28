arduino_led_controller
======================

I'm building a four channel rgb led controller with an arduino.

current
=====
Power is a big one.  When you add up all these led's you are talking a wee bit of juice.

http://learn.adafruit.com/rgb-led-strips/current-draw has some nice pointers that boils down to this:

*  60mA x 10 (ten segments per meter for the 30/LED per meter strip) = 0.6 Amps per meter

This means on our 10A power supply we get (10/0.6) 16.6 meters (55 feet or so) before we go out of spec for the power supply.

At 30/LED per meter, we end up with 16.6*30 or roughly 500 LEDs at FULL brightness.  Any sort of pattern or dimming can extend 
this pretty effectively, half power should be good for 1000 LEDs.  Our four strips are 5 meters each, or 20 meters and 600 LEDs.

To make things safe at full power, we need to drop 4 meters, or 1 meter per strip and we should be ok.

Short of using a computer PSU, this is is folks.

parts (overall)
===============
* 1x adafruit minty (arduino in a can).
* 1x 5v 10amp ps

rough cost: $60

parts (channel)
===============
* 1x 6" rgb cable 
* 1x rgb cabel->four pin connector
* 3x N-channel power mosfet
* 1x 74HC595 shift register

rough cost per channel: $7 ($28 for all 4)

Total cost is roughly $88 sourced from adafruit. 
