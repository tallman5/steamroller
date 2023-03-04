# Steamroller Extruder

**Note: **
All of this is still in beta, please use at your own risk. Thanks!

![OMG Extruder and Steamroller Parts](/images/srs.png "Steamroller")

## Overview
The Steamroller Extruder is a custom adapter to hold the OMG Extruder for various print heads.
The following is a list of the available flavors.

1. Steamroller Stealthburner, SR-SB, for the Stealthburner/Clockwork 2
1. Steamroller Afterburner, SR-AB, for the Afterburner/Clockwork 1 (complete hack, yet works well)
1. Steamroller EVA, SR-EVA, you guessed it, for EVA (not ready for prime-time yet)

Print the files in the STL folder for the appropriate version.
The default STLs have a 4.7mm hole for M3x5x4 threaded inserts.
Since the inserts aren't always easy to get, there are subfolders for other size threaded inserts.
For example, the STLs in the folder ti-5-3 has 5.3mm holes for M3x5.5x4 inserts.
The F360 design has a parameter to globally change the threaded insert hole diameter.
Or, message me and I can create a custom set.

## OMG Extruder Links

This project does not have a donate button. However, if you order the OMG with an affiliate link, you won't pay more and a small commission will go to this project. Thank you!

OMG Home page: [https://www.omgextrd.com/](https://www.omgextrd.com/)

Affiliate Link: [https://amzn.to/3EAxDCI](https://amzn.to/3EAxDCI)

## Why?
During a Voron 2.4 build, I was using the OMG with a bowden tube on the Voron until the Galileo parts came in. There were some great prints coming from the OMG extruder. After installing and tuning the Galileo, I noticed how close the prints were in quality. So, decided to try to go direct drive with the OMG. The Steamroller AB is the result.

## Installation Steps
Everything about this is per the Voron standard, slicer settings, heat set inserts, etc..
The following directions are for the SR-AB. The others are similar.
More detailed instructions to come.

1. Print the parts from the STL folder. Right now, there's only two.
1. Add the heat set inserts
1. Screw the back of the OMG through the motor plate into the stepper motor
   1. For the SR-AB, the motor plate is between the OMG clamshell and the motor
   1. For the SR-SB, the motor is screwed the the clamshell
1. Assemble the rest of the OMG onto the motor plate assembly
1. Position the front of the Steamroller onto the assembly
1. Using the standard carriage -> Clockwork screws, screw the Steamroller to the carriage
1. Cut a piece of PTFE for the Steamroller to the hotend
   1. SR-AB - Mine was 62mm for a v6 hot end
1. Install the fan assembly
1. Edit the printer.cfg, below is what I used with Fluiddd and a Spider v1.2:
      ```
      # Steamroller AB (SB and EVA should be similar)
     rotation_distance: 47.77753134
     microsteps: 16
     full_steps_per_rotation: 760
     gear_ratio: 3:1
     dir_pin: PD6
     ```
1. Do the e-steps calibration and update the rotation_distance
1. Print something!

## How Well Does It Work?
In the following pic, the Galileo is on the left, Steamroller AB on the right. 
They are printed from the same filament spool using same .gcode file. 
The two were printed one right after the other (Steamroller AB installation in between).

![Galileo/Steamroller Calibration Cubes](/images/20220201_082046.jpg "Galileo/Steamroller Calibration Cubes")

## Enjoy!
If you implement it, share it for others!
