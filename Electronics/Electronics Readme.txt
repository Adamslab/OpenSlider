OpenSlider utilizes GRBL1.1 for motion control.

There are quite a few controller boards available that you can use to make your own slider! The current iteration is based on an Arduino UNO with a 4x A4988 Driver shield.

These boards will also work fine:

Arduino Mega + Ramps Combo
MKS Gen
Rambo 1.1a


It is possible to also use other stepper drivers instead of the standard A4988. For example, you could upgrade to the TMC2130 for interpolated microstepping and quieter operation. I chose A4988 due to the low cost.


Bill of Electronic Materials:

3x Nema 17 Stepper Motor
1x 28BYJ-48
1x Arduino UNO + 4 Axis CNC Shield
4x A4988 Stepper Motor Driver
1x 12V 5A Power Supply


UNO + CNC Shield:

Amazon Canada: https://amzn.to/2PT4EC5

Aliexpress: https://www.aliexpress.com/item/cnc-shield-v3-engraving-machine-3D-Printer-4pcs-A4988-driver-expansion-board-UNO-R3-with-USB/32844679218.html
