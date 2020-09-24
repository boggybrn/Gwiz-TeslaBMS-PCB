# Gwiz-TeslaBMS-PCB
The design files for a circuit board to provide the hardware needed to run the Gwiz-TeslaBMS code. This was designed using Designspark PCB and is based around using an STM32 Blue Pill board. Note that there are many copies of this board around which have a CSC version of the STM32F103 device. I was unable to get it working with these - so seek out one with a genuine ST device.

This project is for people fitting Tesla manufactured Mercedes B-Class battery modules to a Reva G-Wiz. Four of these modules will fit under the seats and when wired as two series, two parallel give the desired 48V (nominal). Mostly this project controls the original G-Wiz charger to act appropriately for charging the LiIon battery modules.

The hardware provides:
- An input to detect when the charger is conneced to 240V AC power
- An output to control the charging current
- An output to control the charging voltage (can be used to stop charging)
- An output to control the battery fan used to cool the charger (not tested yet)
- A serial interface to the Mercedes/Tesla battery module BMS slave boards, used to read cell voltages & module temperatures plus to control cell balancing.
- A CAN interface suitable for connecion to a CAN based current sensor e.g. LEM CAB300 (not teted yet)
- A connector to plug in a ESP8266 WiFi/ Web interface module - to give a display of certain values e.g. battery voltage
- A header for connection of an FTDI serial to USB module for configuration and diagnostics

The firmware to run on the Blue Pill can be found at https://github.com/boggybrn/Gwiz-TeslaBMS 

Feel free to use this design as you see fit. Note however that it is offered as is without any warranty or support - it is just something created to get a G-Wiz back on the road and is left here in the hope that it may inspire others!