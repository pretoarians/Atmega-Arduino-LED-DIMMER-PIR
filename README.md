# Atmega Arduino LED DIMMER PIR motion sensor light
This program is useful for creating an energy-efficient lighting system that responds to motion, such as a hallway or security light, with adjustable brightness and automatic turn-off features after a set period of inactivity.


This program controls the operation of a motion-activated LED system using an Arduino platform. Here's an overview of its functionality:

Debug Mode: The program can be run in debug mode, which, when enabled, prints diagnostic information to the serial console. This helps with monitoring the internal state of the program, such as times since motion detection or the LED brightness level.

Motion Detection: The program uses a PIR (Passive Infrared) sensor connected to a specific pin (Pin 2) to detect motion. When motion is detected, the LED (connected to Pin 9 via PWM) turns on and adjusts its brightness accordingly.


