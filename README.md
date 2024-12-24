# Atmega-Arduino-LED-DIMMER-PIR
This program is useful for creating an energy-efficient lighting system that responds to motion, such as a hallway or security light, with adjustable brightness and automatic turn-off features after a set period of inactivity.


This program controls the operation of a motion-activated LED system using an Arduino platform. Here's an overview of its functionality:

Debug Mode: The program can be run in debug mode, which, when enabled, prints diagnostic information to the serial console. This helps with monitoring the internal state of the program, such as times since motion detection or the LED brightness level.

Motion Detection: The program uses a PIR (Passive Infrared) sensor connected to a specific pin (Pin 2) to detect motion. When motion is detected, the LED (connected to Pin 9 via PWM) turns on and adjusts its brightness accordingly.

LED Brightness Control:

Maximum Brightness: The LED can be set to its maximum brightness during the day, controlled by a variable (MAX_PWM_DZIENNE).
Standby Mode: After motion is detected, the LED stays on for a set duration (configured by CZAS_SWIECENIA_PO_WYKRYCIU_RUCHU_MS). After that, it enters a lower brightness "standby" mode (PWM_STANDBY).
Power Off: If no motion is detected for a longer period, the LED is turned off.
Timing and Delays: Various timing mechanisms are in place to control the duration the LED stays on at different brightness levels:

Time Since Last Motion: The program tracks the time since the last motion was detected (CZAS_OD_WYKRYCIA_RUCHU_MS).
Delays for LED Brightness: After detecting motion, the LED gradually increases its brightness over 5 seconds. If no motion is detected, the LED gradually dims until it is turned off.
Functions:

Shine_from_current_point_within_5SEC(): This function gradually increases the LED brightness from its current value to the maximum brightness over 5 seconds.
Main Loop: The main loop constantly checks for motion. If motion is detected, it updates the LED brightness accordingly. If no motion is detected for a set time, it dims the LED or turns it off.
