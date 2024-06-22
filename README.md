This configuration is based on following config https://github.com/charminULTRA/Klipper-Input-Shaping-MK3S-Upgrade?tab=readme-ov-file.
As this project seems no more maintained, I made my own to correct some findings and respect some new Klipper possibilities as for instance native adaptive meshing without Kamp

I suggest to use the Mk3.5 Klipper Profiles like also described in the nice guide of charminULTRA above. As you can see there only less adaptions in the Prusaslicer Profiles are necessary
It´s not neccessary to remove in the Filamnet settings of Prusaslicer the custom Start-G-Code anymore as this config can interprete the Pressure Advance Settings there

Changes:
- New purgeline, no more in the middle of the print bed
- Nozzle supports bed heating correctly
- adaptive meshing activated
- M572 macro added to interpret the PA values from the Prusaslicer Filament Settings
- Stealth Profile introduced (with this profile in Klipper and the Prusaslicer profiles for "structural" print we are still 50% faster then with a normal Mk3s+
- new organisation of the config files. Splitted in printer.cfg and a config folder with the rest of the files
- changed max_accel_to_decel to minimum_cruise_ratio


Prusaslicer Printer Startcode:
M190 S0 ; Prevents prusaslicer from prepending m190 to the gcode interfering with the macro
M109 S0 ; Prevents prusaslicer from prepending m109 to the gcode interfering with the macro
PRINT_START EXTRUDER_TEMP=[first_layer_temperature] BED_TEMP=[first_layer_bed_temperature]
