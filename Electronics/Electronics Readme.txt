OpenSlider utilizes GRBL1.1 for motion control.

There are quite a few controller boards available that you can use to make your own slider! The current iteration is based on an Arduino UNO with a 4x A4988 Driver shield to keep costs down.

These boards will also work fine:

Arduino Mega + Ramps Combo
MKS Gen
Rambo 1.1a


It is possible to also use other stepper drivers instead of the standard A4988. For example, you could upgrade to the TMC2130 for interpolated microstepping and quieter operation. If you are going to use audio from a device mounted directly to the slider, I suggest using TMC2130 drivers to reduce motor noise. I chose A4988 due to the low cost.

Three NEMA 17 stepper motors and one 28BYJ-48 motor are used. Virtually any NEMA 17 motors will work, as long as they are not extremely low power, or extremely overpowered. I suggest NEMA motors rated to at least 20Ncm.

The software utilized is GRBL, and Universal GCode sender (UGS). GRBL is flashed to the Arduino, and UGS is used to send commands to the Arduino from a connected device.

GRBL: https://github.com/gnea/grbl/releases
UGS: https://github.com/winder/Universal-G-Code-Sender


Bill of Electronic Materials:

3x Nema 17 Stepper Motor
1x 28BYJ-48
1x Arduino UNO + 4 Axis CNC Shield
4x A4988 Stepper Motor Driver
1x 12V 5A Power Supply
