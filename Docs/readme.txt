--------------------------------------------------------------------------------
Tiny Power Supply for MSX Computers
Copyright (c) 2024-2025 RBSC
Last updated: 13.07.2025
--------------------------------------------------------------------------------

About
-----

The TinyPSU project was created by RBSC to bring back to life a batch of MSX2 computers, mostly Panasonic FS-A1. Those
computers were lacking original power supply units that made them pretty much unusable. It's a known fact that original
power supplies for those computers are hard to find and even if one is lucky to find one for sale, the price literally
bites. Japanese sellers may easily ask for 70$ for such a power supply. Overseas shipment, local and import taxes can
easily bring the total cost of an original power supply to 100$. But that's not the only problem.

The second problem is that these MSX2 computers have the special 3-pin power socket that was not used in many other MSX
computers. So, reusing power supplies from other MSX computers was never an option. However, similar sockets were used in
some old PC laptops, so it was possible to find an old laptop's power supply in order to utilize its cable to build a
custom power supply for Panasonic FS-A1 or FS-A1 MK2 computers. The TinyPSU project solves this and many other problems.

But the application of this power supply is not only limited to Panasonic FS-A1 and similar MSX computers. Technically,
this power supply can be used with any MSX computer that requires 3 different voltages: +5V, +12V and -12V. For example,
this repository contains a holder for the TinyPSU that could be used with Yamaha YIS 503II, 503III, YIS-604, CX5M, CX11
and similar MSX and MSX2 computers. There's no need to even modify the motherboard in order to fit this power supply into
those computers. Moreover, after installation of this power supply the problem of incompatible mains voltage (100V or 220V)
is also resolved thanks to the universal low-voltage external power supply. Who knows what comes next? Maybe a USB-C option
to power your MSX?

There's the special document-guide in the Docs subfolder of this repository that provides precise instructions on how to
build the TinyPSU in. Please carefully read the "FS-A1_FS-A1MK2_PSU_Guide.pdf" document before doing any repair!


Building in the PSU
-------------------

For certain computers, for example for Yamaha MSX YIS-503 and similar computers, the installation of the TinyPSU is almost
trivial. The PSU needs to be fitted with the power connector similar to the original one (or even the original connector can
be used instead). The installation of the TinyPSU into Panasonic FS-A1 and FS-A1MK2 computers is a totally different thing.
To make space for the TinyPSU certain components must be removed from the mainboard and some additional modifications must
be made to complete the PSU replacement. See the specially created guide document to help you during the installation.

Before starting the repair or upgrade please make sure that you have sufficient skills and all necessary tools. For example,
desoldering components from old circuit boards must be done with extreme caution in order not to damage the main circuit
board. Proper soldering skills are needed to correctly connect the TinyPSU to the mainboard. In addition, you may need
crimping tools, connector shells, crimps and cable insulation stripping tools. If you feel that you don't have enough skills
and tools, leave the work to better equipped people.

As mentioned above, there's a possibility to built the TinyPSU into almost any MSX computer. But every computer may have
its differences, so the installation into each computer or into a family of computers (like Yamaha YIS 503) may require
a different approach. The available 3D models of TinyPSU's holders could be adjusted to be used in other computer models.
If in doubt, seek a piece of advice on MSX.ORG and other forums about vintage electonics.

Where else to find 3D models of TinyPSU's holders:

 - For Panasonic: https://www.thingiverse.com/thing:6987948
 - For Yamaha: https://www.thingiverse.com/thing:6847546


TinyPSU Assembling Notes
------------------------

Please read the following notes carefully:


 - Use only recommended fuse values for the Tinu PSU. Incorrect fuse value may result in a damage to a computer or external
   power supply

 - Use only the recommended external 9V or 12V power supply. Other PSUs, especially cheap ones from AliExpress may result
   in a malfunction of the TinyPSU and/or introduce interference into the audio and video signals of a computer. See the
   installation guide document for the info about the recommened external power supply

 - Use only recommended voltage ratings for electrolytic capacitors. Incorrect voltage rating may result in blown or leaked
   capacitors and other anomalies

 - Use only recommended suppressor diode with breakdown voltages from 5.6V up to 6.4V. Higher or lover breakdown voltages
   may result in a non-working power supply or may damage your MSX computer!

 - Use only the recommended coil types and coil values. Incorrect coil type or its value may result in severe pulsation
   on the power rails that may prevent a computer from operating properly

 - When selecting wires for connecting the TinyPSU to the mainboard, please make sure that they can hold up to 2A current,
   otherwise your computer may be starving for power if too thin or low quality wires are used

 - The ST1S10 step-down voltage regulator IC may get hot during its operation. The lead frame die pad of the ST1S10 is
   exposed at the bottom of the package and must be soldered directly to a properly designed thermal pad on the PCB. This
   means that soldering must be done either with hot air from the reworking station or with the help of the infrared
   reworking station that heats the board from the bottom. The heat from the IC will be dissipated via the carefully
   designed thermal pad

 - The XL6007E1 DC-DC convertor IC may get hot during its operation. Unlike the ST1S10, it doesn't have a die pad on the
   bottom to be soldered onto the board. So, it's recommended to apply good thermal paste onto the bottom of the IC before
   soldering its 8 pins to the circuit board

 - While the +12V circuit was designed for up to 2A load, the total -12V circuit's load must not exceed 100mA. Most of MSX
   computers and cartridges will not exceed this load during normal operation. This limitation comes from the VA-1212S 1W
   DC-DC converter that is installed to produce -12V for the MSX power rail

 - Though the circuit board is designed to dissipate the heat from active elements, it's not recommended to install the
   TinyPSU in poorly ventilated tight spaces, as well as near other sources of heat. The step-down converter may heat up
   to 60 degrees Celsius, the -12V DC-DC converter may heat up slightly more. During the testing phase the TinyPSU was
   tested for many hours with the maxumum allowed load with constant temperature monitoring and no excessive heating has
   been observed


IMPORTANT!
----------

The RBSC provides all the files and information for free, without any liability (see the disclaimer.txt file). The provided
information, software or hardware must not be used for commercial purposes unless permitted by the RBSC. Producing a small
amount of bare boards for personal projects and selling the rest of the batch is allowed without the permission of RBSC.

When the sources of the tools are used to create alternative projects, please always mention the original source and the
copyright!


Contact information
-------------------

The members of RBSC group Tnt23, Wierzbowsky, Pyhesty, Ptero, GreyWolf, SuperMax, VWarlock, ALSP and DJS3000 can be contacted
via the group's e-mail address:

info@rbsc.su

The group's coordinator could be reached via this e-mail address:

admin@rbsc.su

The group's website can be found here:

https://rbsc.su/
https://rbsc.su/ru

The RBSC's hardware repository can be found here:

https://github.com/rbsc

The RBSC's 3D model repository can be found here:

https://www.thingiverse.com/groups/rbsc/things

-= ! MSX FOREVER ! =-
