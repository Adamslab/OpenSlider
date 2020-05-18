# Materials List
openslider.xyz

## Printing

PETG or ABS is reccomended.
No support material is needed. Calibrating your bridging settings will help produce cleaner prints.

0.2mm Layer Height, 3 to 5 perimeters and 25% infill is reccomended. Use your own judgement.

## Nuts/Bolts:

An exact list of required fasteners is coming in the future.

Development of OpenSlider is moving towards four primary fastener types: M3x10mm, M3x20mm, M3x30mm and M5x30mm.


* 5x M5x30mm Bolts
* 3x M3x30mm Bolts
* 1x M3x15mm Bolt
* 5x M5 Nuts
* 4x M3 T-Nuts
* Assorted M3 bolts + hexagonal nuts https://s.click.aliexpress.com/e/_sIpZ55
* 1x GT2 Idler Pulley - 3mm Bore (Toothed)(For X-Axis) - https://s.click.aliexpress.com/e/_dZw7ybJ


## Frame:

The X-Axis runs along a V-Sot 2040 aluminum extrusion. The longer the extrusion, the more travel distance you will have.

The slider assembly takes approximatly 120mm off of the travel distance.

A 500mm extrusion will give you approximately 380mm of travel.

https://s.click.aliexpress.com/e/_sMJLWJ



## Roller Carriage Wheels

3x V-Slot or T-Slot roller wheels are used for the X-Axis roller carriage.

For T-Slot rail,  3x Option B or similar roller wheels are used: https://s.click.aliexpress.com/e/_rJTbgF



## GT2 Belt

GT2 6mm belt is used.
The length of belt you will need for the X-Axis is double the length of the extrusion that you're using for the X-Axis plus ~50mm.
So for a 500mm X-Axis, you need approximately 1050mm of belt to have enough.

The Y-Axis and Z-Axis uses GT2 belt loops.
The tensioning system will work with 250mm to 264mm belt loops. 250mm is reccomended.

https://s.click.aliexpress.com/e/_rQ35Lp

https://s.click.aliexpress.com/e/_sOoTyx



## Bearings:

Bearings used are 608RS. 8mm ID, 22mm OD

Like these: https://s.click.aliexpress.com/e/_s3uaUI


## Electronics:

For the main branch, an SKR 1.3 is used as the main controller and TMC2130 drivers are used for the motors.

A 12864 LCD (RepRapDiscount Full Graphic Smart Controller) is used for a display, and local controls with SD functionality.

12V 5A power supply.

(Optional) An ESP8266 module can be added to provide control over WIFI

SKR 1.3 Mainboard with LCD controller and motor drivers: https://s.click.aliexpress.com/e/_sN61d8

SKR 1.3 without LCD: https://s.click.aliexpress.com/e/_sc29Y2

ESP8266: https://s.click.aliexpress.com/e/_dUlDbDn



There are many alternatives for motion control. An SKR board is chosen due to the versatility and price point.

Different stepper motor drivers provide different benefits. 

* A4988 are low cost with reliable performance and 1/16 stepping
* DRV8825 offer high current capability and 1/32 stepping. 
* TMC2130 have sensorless homing, stealthchop and 1/256 stepping. 
* TMC2209 have higher current capability, improved sensorless homing and stealhchop and 1/256 stepping. 

There are lots of other options out there. The choice is up to you, your budget and what features you want.


## Motors

Nema 17 motors are used. One motor is needed for each axis. If you just want X and Y motion, you will only need two motors.

If you expect to do vertical movements with a DSLR, or rapid back and forth movements with high acceleration, 42Ncm or higher is reccomended. For a cellphone, action camera or PiCamera you can get away with 13-20Ncm motors.

https://s.click.aliexpress.com/e/_sd4SLV


## Software

The camera slider runs on a branch of Marlin Bugfix 2.0. Marlinfw.org

The version of Marlin included with OpenSlider is configured for the SKR1.3 and TMC2130 drivers. If you are using a different control board or stepper drivers you will have to manually configure Marlin to support your hardware.


It is reccomended to flash Marlin to the SKR using PlatformIO and Visual Studio Code.






---------------------------------------------
----
----------------------------------------------
----
----------------------------------------------


# OpenSlider Legacy (Older Versions)
Arduino UNO + GRBL1.1 Shield for motion control.

This is the current control board setup used:
http://osoyoo.com/2017/04/07/arduino-uno-cnc-shield-v3-0-a4988/

I purchased mine through Aliexpress, though it is a widely available setup. You can find this Uno + CNC shield kit on most online retailers, like Amazon, eBay, etc.

There are many other boards available that will accomplish the same thing. The reason I chose the UNO + 4x A4988 setup is because it is extremely affordable, simple to use and it's widely available.

It is possible to also use other stepper drivers instead of the standard A4988. For example, you could upgrade to the TMC2130 for interpolated microstepping and quieter operation. If you are going to use audio from a device mounted directly to the slider, I suggest using TMC2130 drivers to reduce motor noise. I chose A4988 due to the incredibly low cost.

Three NEMA 17 stepper motors are used for motion control. Virtually any NEMA 17 motors will work, as long as they are not extremely low power, or extremely overpowered. I suggest NEMA motors rated to at least 20Ncm.

The software utilized is GRBL, and Universal GCode sender (UGS). GRBL is flashed to the Arduino, and UGS is used to send commands to the Arduino from a connected device.

## Software (Legacy)

GRBL: https://github.com/gnea/grbl/wiki
UGS: https://github.com/winder/Universal-G-Code-Sender

## Belts (Legacy)
The slider uses GT2 timing belts with 2mm pitch. You can use 6mm or 8mm width belts, whichever you prefer. The X-Axis requires one long piece of belt, and the other axis require 250mm continuous belts. You can make continuous belts by attaching the ends of a straight piece of belt cut to the right size, with an adhesive like CA glue.

## Electronics: (Legacy)
3x Nema 17 Stepper Motor
1x Arduino UNO + 4 Axis CNC Shield
4x A4988 Stepper Motor Driver
1x 12V 5A Power Supply
