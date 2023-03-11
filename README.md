# Steamroller

![OMG Extruder and Steamroller Parts](/images/srs.png "Steamroller")

<div style='border: 1px solid #997404; border-radius: 5px; background-color: #fff3cd; padding: 15px; color: #997404;'>
   <strong>Note: </strong>These are still in testing. Please use at your own risk. Create an issue if needed. Thanks!
</div>

## Overview
The Steamroller is a custom adapter to hold the OMG Extruder for various print heads.
The following is a list of the available flavors.

1. Steamroller Stealthburner, SRSB, for the Stealthburner/Clockwork 2
1. Steamroller Afterburner, SRAB, for the Afterburner/Clockwork 1
1. Steamroller EVA, SREVA, you guessed it, for EVA, coming soon!

Print the files in the STL folder for the appropriate version.
The default STLs have a 4.7mm hole for M3x5x4 threaded inserts.
Since the inserts aren't always easy to get, there are subfolders for other size threaded inserts.
For example, the STLs in the folder ti-5-3 has 5.3mm holes for M3x5.5x4 inserts.
Want a different threaded insert size?
Create an issue here and I can create a custom set.

## OMG Extruder Links

This project does not have a donate button.
However, if you order the OMG with an affiliate link, you won't pay more and a small commission will go to this project.
Thank you!

Affiliate Link: [https://amzn.to/3EAxDCI](https://amzn.to/3EAxDCI)

## Why?
During a Voron 2.4 build, I was using the OMG with a bowden tube on the Voron until the Galileo parts came in.
There were some great prints coming from the OMG extruder.
After installing and tuning the Galileo, I noticed how close the prints were in quality.
So, decided to try to go direct drive with the OMG.
The Steamroller AB is the result.

## Installation Steps
Everything about this is per the Voron standard, slicer settings, heat set inserts, etc..

1. Gather parts from the BOM, there's a BOM for each flavor
1. Print the parts
   1. Yellow's not required :smile:, just used it on renders following the Steamroller theme
   1. Front and back found in the STL folder
   1. The 2- or 3- hole chain anchor from the Voron Clockwork 2 found [here](https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Clockwork2)
   1. If using the SRSB, the cable cover from the Voron Clockwork 2 found [here](https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Clockwork2)
1. Add the heat set inserts
1. Install the cable chain anchor to the back
1. For the SRSB, install the cable cover to the back
1. If installing a NEMA17 on the SRAB, push the motor through the back before attaching the motor to the OMG
1. Place the OMG in the Steamroller front
1. Screw the back to the front
1. Install a piece of PTFE for the Steamroller to the hotend
   1. SRAB - Mine was 62mm for a v6 hot end
1. Mount the Steamroller to the carriage
1. Install the fan assembly
1. Edit the printer.cfg, below is what I used with Klipper/Fluiddd/Spider v1.2:
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
In the following pic, the Galileo is on the left, SRAB on the right. 
They are printed from the same filament spool using same .gcode file. 
The two were printed one right after the other (SRAB installation in between).

![Galileo/Steamroller Calibration Cubes](/images/20220201_082046.jpg "Galileo/Steamroller Calibration Cubes")

## Got A Request?
Have something you think would be useful?
Feel free to create an issue here for something you may want added.
Such as, threaded inserts for PCBs.
Most of my stuff is at a minimum, so, I may not have added something you'd find useful.

## Enjoy!
If you implement it, send me a pic and I'll share it for others!
