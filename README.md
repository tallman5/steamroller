# Steamroller Extruder
Not ready for prime time, this is a work in progress! Use at own risk!

## TLDR
The Steamroller extruder is a Voron Clockwork, modified to hold an OMG Extruder. In the STL folder, print only the files starting with steamroller. The others are of a single "block" made from the original Clockwork. The block became the starting point for the Steamroller.

![OMG Extruder and Steamroller Parts](/images/20220129_080903.jpg "Steamroller Extruder Parts")

## OMG Extruder Links
Home page: [https://www.omgextrd.com/](https://www.omgextrd.com/)

This project does not have a donate button. However, if you order the OMG with one of the affiliate links, you won't pay more and a small commission will go to this project. Thank you!

### Affiliate Links:
| |Amazon|AliExpress|
|-|------|----------|
|w\ Stepper|[https://amzn.to/3evmbuK](https://amzn.to/3evmbuK)|[https://s.click.aliexpress.com/e/_ApIpiY](https://s.click.aliexpress.com/e/_ApIpiY)|
|w\o Stepper|[https://amzn.to/32xOlTq](https://amzn.to/32xOlTq)|[https://s.click.aliexpress.com/e/_9vAmFe](https://s.click.aliexpress.com/e/_9vAmFe)|

## Why?
During a Voron 2.4 build, I was using the OMG with a bowden tube on the Voron until the Galileo parts came in. There were some great prints coming off the Voron. After installing and tuning the Galileo, I noticed how close the prints were in quality. So, decided to try to go direct drive with the OMG. The Steamroller is the result.

## Installation Steps
Everything about this is per the Voron standard, slicer settings, heat set inserts, etc..

1. Print all the parts starting with "steamroller-" from the STL folder. Right now, there's only two
1. Add the heat set inserts, seven in total
1. Screw the back of the OMG through the motor plate into the stepper motor
1. Assemble the rest of the OMG onto the motor plate assembly
1. Position the front of the Steamroller onto the assembly
1. On the stepper, cut the end of the wires and crimp ends to match your wiring harness or PCB
1. Using the standard carriage -> Clockwork screws, screw the Steamroller to the carriage
1. Cut a piece of PTFE, mine was 62mm for a v6 hot end
1. Install the fan assembly
1. Edit the printer.cfg, below are what I used with Fluiddd and a Spider v1.2:
      ```
      # Steamroller
     rotation_distance: 47.77753134
     microsteps: 16
     full_steps_per_rotation: 760
     gear_ratio: 3:1
     dir_pin: PD6
     ```
1. Do the e-steps calibration and update the rotation_distance
1. Print something!

## How Well Does it Work?
In the following pic, the Galileo is on the left, Steamroller on the right. They are printed from the same filament spool using same .gcode file. The two were printed one right after the other (Steamroller installation in between).

![Galileo/Steamroller Calibration Cubes](/images/20220201_082046.jpg "Galileo/Steamroller Calibration Cubes")

Yes, there's some ringing. I had done a manual ringing tower with the Galileo (along with pressure advance, etc.). I did not recalibrate or clear the settings before the Steamroller.

## Known Issues
1. The cable chain mount could be thicker. The heat set inserts and screws protrude through the bottom.
1. No cable cover... yet. Maybe the Galileo one works with a longer screw through the motor mounting?

## Enjoy!
If you implement it, share it for others!
