OpenSlider utilizes GRBL1.1 for motion control. 

There are quite a few controller boards available that you can use to make your own slider! Any 4-axis controller that supports GRBL will work.

The current iteration is based on an Arduino UNO with a 4x A4988 Driver shield.

Amazon Canada: https://amzn.to/2PT4EC5
Aliexpress: https://www.aliexpress.com/item/cnc-shield-v3-engraving-machine-3D-Printer-4pcs-A4988-driver-expansion-board-UNO-R3-with-USB/32844679218.html

The software utilized is GRBL, and Universal GCode sender (UGS). GRBL is flashed to the Arduino, and UGS is used to send commands to the Arduino from a connected device.

GRBL: https://github.com/gnea/grbl/releases
UGS: https://github.com/winder/Universal-G-Code-Sender


Bill of Electronic Materials:

3x Nema 17 Stepper Motor
1x 28BYJ-48
1x Arduino UNO + 4 Axis CNC Shield
4x A4988 Stepper Motor Driver
1x 12V 5A Power Supply
