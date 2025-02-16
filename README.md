# RPSpatCNC
Take the wonderful PicoBOB-DLX from Expatria Technologies, Stir in the RP2350B example board from Raspberry Pi Foundation.  Add USB C PD EPR and this may be what you get.

# Sources of inspiration

https://github.com/Expatria-Technologies/PicoBOB-DLX

PicoBOB-DLX from Expatria Technologies.  An RP2040 based CNC controller for either GRBL HAL, or using the [Remora](https://github.com/scottalford75/Remora) firmware, connect via ethernet to a computer running Linux CNC

https://www.raspberrypi.com/documentation/microcontrollers/silicon.html

Raspberry Pi Foundation released in 2023 the Raspberry Pi Pico 2 usint the new RP2350A micro controller, at the same time, they announced the RP2350 series of micro controllers.

In the documentation for the RP2350, there is a document and files for creating an example MCU board using the RP2350B.  The Schematic and PCB were used from the KiCAD files posted on the Raspberry Pi website.

The RP2350B has 18 more pins than the original RP2040, as well as more RAM and an additional PIO state machine.

[USB C PD](https://www.usb.org/usb-charger-pd)

USB C PD 3.1 has a EPR (Extended Power Range) specification that allows up to 240W of power to be requested by a sink and sent by a source at 45V and 5A.  A fairly good set of CNC Axis can be made with in that.  Spindles will require additional power supplies still however.

# Software used

KiCAD 8.0, as well as a little bit of Fusion 360 for a locking mechanism for the USB C connections.

# The Rest of the Story

At the time of writing this (2025/02/13) this project consists of the KiCAD files and a Fusion 360 object.  To take it further, I will need to aquire an RP2350B, and get the PCB made.  Partial assembly by the fab house might get done, especially if it makes aquasition of some of the parts easier.

I'm trying to make this as compatible as possible with the PicoBOB-DLX, but the firmware from that for Remora and GRBLHal will not work because I have changed some of the pins.  As time permits, I will create projects for the firmwares.  I might even see if uCNC can be ported.
