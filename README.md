# MamaMatrix
A few code examples to quickly experiment with LED matrices prepared for a workshop at the UAL Creative Computing Institute.
The aim of the workshop was to develop ideas around a physical low resolution display by quickly prototipe and simulate ideas. 
A small framework to facilitate prototyping was developed and used during the workshop.

[Event presentation](http://one.ca-n.in)\
[Document 1 on CreativeApplications](https://www.creativeapplications.net/can-events/document-1-cans-new-event-seriesexamines-cross-disciplinary-practice/)

# Part list
- RGB LED matrix 32x64 P5 (P5 means that the LED pitch is 5mm)
- HUB75 ribbon cable 
- 5V power supply (3-4A minimum) plus cables
- Teensy development board 3.5 or 3.6 (a Teensy 3.2 will do but has limited memory)
- [SmartLed shield](https://docs.pixelmatix.com/SmartMatrix/) (not strictly necessary but handy to quickly connext the micro-controller)

# Software requirements
- [Arduino IDE](https://www.arduino.cc/en/Main/Software) 
- [Processing](https://www.processing.org/download/)

# Examples

All the examples rely on the [SmartMatrix](https://github.com/pixelmatix/SmartMatrix) library for Arduino. The many features of the library are not demonstrated: the libraray comes with an extensive collection of examples.

__a1_single_pixel__\
Smallest example program that runs directly on the microcontroller.
A few LEDs are activated “manually”.

__a2_single_pixel_animated__\
Another simple example with some moving LEDs.

__a3_serial_rgb_slave__\
A slave program that forwards incoming pixel data from the serial port to the LED panels.
The code is unoptimized but runs smooth at 60fps on a single matrix and aroun 30fps on 4 matrices.
The following Processing examples encodes some pixels from the canvas or a render target.

__p1_serial_rgb_send_canvas__\
A simple example that grabs all the pixels from the Processing canvas and sends them to the sieral port.

__p2_serial_rgb_send_webcam__\
Same as above but with a live webcam.

__p3_serial_rgb_preview__\
A slightly more structured example with a better (aka bigger) preview.
The slave is always configured to as a stack of matrices. The master program can be configured to slice the canvas accordingly.

__p4_serial_rgb_multi_anims__\
A demonstration running several scenes from a single Processing sketch.

Note:
- Read the code comments for some additional informations.
- Slave and master programs must be configured manually (an automatic configuration is out of scope but could be implemented).






