# RW_EM
Repository containing all Eurorack compatible modules designed and released under the Die Rechenwerke name.

## License and warranty (VERY IMPORTANT!!!)

**All modules (schematics, pcb layouts and panels) are distributed WITHOUT ANY EXPRESS OR IMPLIED
WARRANTY, INCLUDING OF MERCHANTABILITY, SATISFACTORY
QUALITY AND FITNESS FOR A PARTICULAR PURPOSE. 
All modules are released under the CERN-OHL-S v2+ license. Please see
the CERN-OHL-S v2 or newer for applicable conditions.**

## Directories

- The modules directory contains all design files regarding Eurorack modules
- The KicadLibs directory is made up of all Kicad libraries used with the design files apart from standard ones shipped with Kicad
- PanelResources includes svg files used in almost all panel designs (file content might not be to scale, use them with caution)

## Building modules

### PCB

To build a module just generate the necessary gerber files and let the PCB be manufactured by JLCPCB or some other service.
You can also build modules according to the schematics on a perfboard although I never did that.

### Panels

![Panel Picture](https://github.com/sunfl0w/RW_EM/blob/master/Modules/VCOs/RW_EM_VCO_A/RW_EM_VCO_A.jpg?raw=true)

All panels adhere to the standard presented here: https://doepfer.de/a100_man/a100m_e.htm .
Panels can be manufactured by some laser cutting service, but I only used and tested Sculpteo in Europe so far.
Panels may have a maximum thickness of 3mm. I only tested black acrylic (3mm) for now and it worked out great so far.
Notice that the panels svg files do not contain colors for differentiating cuts and engravings.
For hints look at the dxf panel files in QCAD or a similar program as they specify a layer for each line.
Generally the panel's outlines and the mounting holes are cut, as are all holes for switches, LEDs and potentiometers.
All text is only vector engraved and potentiometer scales are vector and surface engraved.

Tip:
To make the text on a black acrylic panel more visible use some white acrylic paint for all engravings.
Use a cotton swab or something similar to get paint into all engraved lines. Then wipe the panels off with paper towels (do not use water).
The paint will only stick to the engraved surface and can easily be wiped off everywhere else.

### General assembly

Please check beforehand if your components will fit into the PCB before assembly!
Especially switches can be a tricky at times.

When assembling a module, start with the back of the PCB as most components are to be placed there.
Put vertically smaller parts in first and solder them one by one. Progress to larger and larger parts as you go.
Jacks, switches and potentiometers and LEDs on the front go last.

Tip:
Use sockets for ICs. If they get damaged you can just put a new one in easily.

Notice:
Look out for the RW_EM_A(DS)R_EG_A module. The 10pin Eurorack power socket and a 3.5mm jack conflict as both share some common PCB space.
In this case the 3.5mm jack should go in first and then the proceed with the Eurorack power socket.

Also make sure that all resistors with a * are matched in pairs. All pairs should be easy to see in the relevant schematic.
Generally resistors with 1% accuracy are already good enough and need no matching.

## Frequently used components

The following components are frequently used in all modules but are more or less only used for synthesizer related projects and therefore harder to source:

- PJ301M-12 and PJ398SM => Can be easily sourced from www.thonk.co.uk. I always use them together with the hex nuts
- PJ366ST => Can be easily sourced from www.thonk.co.uk. Only used in the RW_EM_OUT_A module so far
- Mini toggle switches with pins (or solder lugs) => Can be easily sourced from www.thonk.co.uk. Do not confuse them with sub-miniature switches. Look into the schematics to see if an ON-ON or an ON-OFF-ON switch are needed. Larger switches with lugs will probably not fit into most modules. Some modules like the RW_EM_LFO_A use a footprint that fits switches with lugs, but the pin switches will also fit. To be sure if a switch will fit, look at the used footprint dimensions and compare them with the switch you want to use.
- SONG HUEI R0904N 9mm => Can be easily sourced from www.thonk.co.uk. The tall ones are used in all modules!
- Alpha 9mm => Can be easily sourced from www.thonk.co.uk. Normal sized vertical ones are used in all modules!
- 'Erica Synth' style knobs => Can be easily sourced from www.thonk.co.uk. The knobs are used in combination with the alpha pots. The panels are designed for the medium sized knobs only!

All other parts are "standard". Just follow the footprint sizes specified in all schematics.