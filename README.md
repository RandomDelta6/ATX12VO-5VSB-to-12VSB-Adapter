# Introduction

in progress
# Project Status
Under development

# Schematic
<img src= "insert"  width="750"> 

# PCB
<img src="https://user-images.githubusercontent.com/53912269/231196245-f957f703-b3f5-4f59-a1fb-1b842249071a.png" width ="250">        

PCB Front View



<img src="https://user-images.githubusercontent.com/53912269/231196644-56486391-207f-436a-bc93-ca6299a9212b.png" width ="250">

PCB Back View



# Usage

Wave solder all SMD components on the front side of the board. Proceed to solder in the diode and inductor on the back. Thread in the cables from the back and solder onto the front side, ensure enough solder flows to make a solid connection through the plated through hole and solder flows across to the exposed contact on the back side. Please note that +12V and GND terminals are pretty close, ensure the terminals are not bridged during soldering.

It is to be noted that +5VSB commences at the PSU Connector end and terminates at this board while +12VSB originates at this board and continues to the ATX 12VO Motherboard Connector. +12V and GND wires are to run across the cable from the PSU connector end to the motherboard connector end and the +12V and GND connections for this board may use wires spliced in with the +12V and GND wires running across the cable or have dedicated wires run through the PSU connector end to the +12V and GND terminals of this board.

# Notes

This board prioritises small form factor above all else and as such will have a performance penalty as opposed to the reference two layer, single sided component layout with global ground net on bottom layer. 

Mounting the magnetic component (Inductor) directly on the otherside of the controller introduces significant noise and coupling. As such a 4 layer PCB is required for isolation which is achieved by flooding ground in the middle two copper layers as well as underneath the inductor on the bottom layer. This should provide significant shielding to signal lines and the throughly stitched ground planes should ensure low impedance across ground net. This minimises the magnetic effect but does not completely isolate it, as such a nominal coil whine is to be expected.

The reference design might be cheaper as it utilises 2 layers as opposed to 4 layers in this design, but the cost difference should be negligible on a per unit basis when panelized due to the smaller board footprint in this design which would net more boards from a similar sized panel. Thorough use of vias in this design is necessary for proper signal integrity even though it might increase expense. Thick signal traces are used wherever necessary to minimise the inductive effect of the tracks for high frequency signals.


Although I am pretty confident the board should work, you might still wish to have the board verified by a professional. I am not particularly confident about the values of C4 and C10.

Couldn't find a proper model for Inductor L1 and Diodes D1 and D2, so they are missing on the PCB views.

This project was made with Kicad 7.0


# Disclaimer
This board has not been printed and tested physically to verify functionality. I do not assume any liability for the materials, information and opinions provided on, or available through, this project. I disclaim any liability for injury, death or damages resulting from the use thereof. Modify or work on it at your own risk.

# Licensing
All PCB design files and hardware are released under the [Creative Commons Attribution Share Alike 4.0 license](https://choosealicense.com/licenses/cc-by-sa-4.0/). 

Commercial Usage strictly disallowed.
