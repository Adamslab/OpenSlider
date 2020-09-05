# Materials List

Build tutorial: 

https://www.youtube.com/watch?v=6d8_oJsUrao (Work in progress)


## Printing The Frame
<img src="https://user-images.githubusercontent.com/45019189/82775396-f59a6d00-9e1d-11ea-9ca9-89be5ede4bb7.jpg" width="700">

The majority of the slider assembly is 3D printed. PETG or ABS is reccomended.

No support material is needed. Calibrating your bridging and horizontal expansion settings will help produce cleaner prints.

0.15mm or 0.2mm Layer Height, 3 to 5 perimeters and 25% infill is reccomended. Use your own judgement.

All of the M3 nut traps are undersized by ~0.1mm, to grab onto the nuts to stop them from falling out during assembly.
You will have to force the M3 nuts into place. This is normal. 
If your printer is poorly calibrated, you might have to use a soldering iron to set the M3 nuts.


The M3 and M5 bolt holes are oversized by at least 0.2mm.
If you're finding that the bolt holes are coming out undersized, you need to calibrate your printer or adjust your horizontal expansion settings. You can also size the holes with a drillbit.

See something you want changed? You can do it yourself using the included .STEP and .F3D files.
There is a .STEP file of the entire slider assembly included in the 3D Models directory.
The slider assembly is free forever with no guarantees or warranty of any kind.


## Nuts/Bolts:

An exact list of required fasteners is coming in the future.
Development of OpenSlider is moving towards four primary fastener types: M3x10mm, M3x20mm, M3x30mm and M5x30mm.


* 5x M5x30mm Bolts
* 3x M3x30mm Bolts
* 1x M3x20mm Bolt
* 5x M5 Nuts
* 5x M3 T-Nuts
* Assorted M3 bolts + hexagonal nuts https://s.click.aliexpress.com/e/_sIpZ55
* 1x GT2 Idler Pulley - (3mm Bore - 20 Teeth)(For X-Axis Idler) - http://s.click.aliexpress.com/e/_d8NUSUX
* 3x GT2 Timing Gear (5mm Bore - Need 1 for each axis of motion) - http://s.click.aliexpress.com/e/_BfZtUX7v

M3 washers (7mm OD) are suggested to help prevent deformation of printed parts but are not required.




## X-Axis Rail:

The X-Axis runs along a V-Slot 2040 aluminum extrusion. You can put two 2020 extrusions together if you do not have a 2040 extrusion.
The longer the extrusion, the more travel distance you will have.

The slider assembly takes approximatly 120mm off of the travel distance.

A 500mm extrusion will give you approximately 380mm of travel.

https://s.click.aliexpress.com/e/_sMJLWJ


## Roller Carriage Wheels

3x V-Slot roller wheels are used for the X-Axis roller carriage.

3x Option B or similar roller wheels are used:

https://s.click.aliexpress.com/e/_rJTbgF


## GT2 Belt

GT2 6mm belt is used.
The length of belt you will need for the X-Axis is double the length of the extrusion that you're using for the X-Axis plus ~50mm.
So for a 500mm X-Axis, you need approximately 1050mm of belt to have enough.

http://s.click.aliexpress.com/e/_d9epYdt

The Y-Axis and Z-Axis uses GT2 belt loops.
The tensioning system will work with 250mm to 264mm belt loops.

https://s.click.aliexpress.com/e/_rQ35Lp

https://s.click.aliexpress.com/e/_sOoTyx



## Bearings & Idler:

Bearings used are 608RS. 8mm ID, 22mm OD

The Y-Axis and Z-Axis use 3 to 4 bearings each (Depending on belt loop length)

Like these: https://s.click.aliexpress.com/e/_s3uaUI

The X-Axis uses a 3mm bore 20 tooth idler pulley: http://s.click.aliexpress.com/e/_d8NUSUX



## Electronics:

For the main branch, an SKR 1.3 is used as the controller with TMC2130 stepper motor drivers.

A 12864 LCD (RepRapDiscount Full Graphic Smart Controller) is used for a display with local controls with SD functionality.

12V 5A power supply to power the slider. 5 Amps is the suggested minimum for 3-axis motion.

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

If you expect to do vertical movements with a DSLR, or rapid back and forth movements with high acceleration, 42Ncm or higher is reccomended. For a cellphone, action camera or PiCamera you can use weaker motors.

https://s.click.aliexpress.com/e/_sd4SLV


## Software

The camera slider runs on a branch of Marlin Bugfix 2.0. Marlinfw.org

The version of Marlin included with OpenSlider is configured for the SKR1.3 and TMC2130 drivers. If you are using a different control board or stepper drivers you will have to manually configure Marlin to support your hardware.

It is reccomended to flash Marlin to the SKR using PlatformIO and Visual Studio Code.

https://code.visualstudio.com/


If you decide to use an Arduino UNO/Nano or a similar lower cost setup, you will want to use GRBL1.1 for control instead of Marlin.
