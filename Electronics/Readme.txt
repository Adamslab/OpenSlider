OpenSlider utilizes an Arduino UNO + GRBL1.1 Shield for motion control.

This is the current control board setup used:
https://www.aliexpress.com/w/wholesale-Arduino-UNO-CNC-A4988.html

There are many other boards available that will accomplish the same thing. The reason I chose the UNO + 4x A4988 setup is because it is extremely affordable, simple to use and it's widely available.


It is possible to also use other stepper drivers instead of the standard A4988. For example, you could upgrade to the TMC2130 for interpolated microstepping and quieter operation. If you are going to use audio from a device mounted directly to the slider, I suggest using TMC2130 drivers to reduce motor noise. I chose A4988 due to the incredibly low cost.

Three NEMA 17 stepper motors and one 28BYJ-48 motor are used. Virtually any NEMA 17 motors will work, as long as they are not extremely low power, or extremely overpowered. I suggest NEMA motors rated to at least 20Ncm.


Bill of Electronic Materials:

3x Nema 17 Stepper Motor
1x 28BYJ-48 (Modified to be a Unipolar motor)
1x Arduino UNO + 4 Axis CNC Shield
4x A4988 Stepper Motor Driver
1x 12V 5A Power Supply
