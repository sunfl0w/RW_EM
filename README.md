# RW_EM
Repository containing all Eurorack compatible modules designed and released under the Die Rechenwerke name

## Modules

The modules directory contains all Eurorack modules.

## Building modules

### PCB

To build a module just generate the necessary gerber files and let the PCB be manufactured by JLCPCB or some other service.
You can also build modules according to the schematics on a perfboard although I never did that.

### Panels

All panels adhere to the standard presented here: https://doepfer.de/a100_man/a100m_e.htm
Panels can be manufactured by some laser cutting service, but I only used and tested Sculpteo in Europe so far.
Panels may have a maximum thickness of 3mm. I only tested black acrylic (3mm) for now and it worked out great so far.
Notice that the panels svg files do not contain colors for differentiating cuts and engravings.
For hints look at the dxf panel files in QCAD or a similar program as they specify a layer for each line.
Generally the panel's outlines and the mounting holes are cut, as are all holes for switches, LEDs and potentiometers.
All text is only vector engraved and potentiometer scales are vector and surface engraved.

Tip:
To make the text on a black acrylic panel more visible use some white acrylic paint for all engravings.
Use a cotton swab or something similar to get paint into all engraved lines. Then wipe the panels off with paper towels (do not use water).
The paint will only stick to the engraved surface and can be easily wiped off everywhere else.

### General assembly

Please check beforehand if your components will fit into the PCB before assembly!
Especially switches can be a tricky at times.

When assembling a module, start with the back of the PCB as most components are to be placed there.
Put vertically smaller parts in first and solder them one by one. Progress to larger and larger parts as you go.
Jacks, switches and potentiometers and LEDs on the front go last.

Look out for the RW_EM_A(DS)R_EG_A module. The 10pin Eurorack power socket and a 3.5mm jack conflict as both share some common PCB space.
In this case the 3.5mm jack should go in first and then the proceed with the Eurorack power socket.

Tip:
Use sockets for ICs. If they get damaged you can just put a new one in easily.

## Frequently used components

The following components are frequently used in all modules but are more or less only used for synthesizer related projects and therefore harder to source:

- PJ301M-12 and PJ398SM => Can be easily sourced from www.thonk.co.uk
- PJ366ST => Can be easily sourced from www.thonk.co.uk. Only used in the RW_EM_OUT_A module so far
- Mini toggle switches with pins (or solder lugs) => Can be easily sourced from www.thonk.co.uk. Do not confuse them with sub-miniature switches. Look into the schematics to see if an ON-ON or an ON-OFF-ON switch are needed. Larger switches with lugs will probably not fit into most modules. Some modules like the RW_EM_LFO_A use a switches  with lugs instead of pins but the pin switches will also fit. To be sure if a switch will fit, look at the used footprint dimensions and compare the with the switch you want to use.
- SONG HUEI R0904N 9mm => Can be easily sourced from www.thonk.co.uk. The tall ones are used in all modules!
- Alpha 9mm => Can be easily sourced from www.thonk.co.uk. Normal sized vertical ones are used in all modules!
- 'Erica Synth' style knobs => Can be easily sourced from www.thonk.co.uk. The knobs are used in combination with the alpha pots. The panels are designed for the medium sized knobs only!

All other parts are "standard". Just follow the footprint sizes specified in all schematics.