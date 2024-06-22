This configuration is based on following config https://github.com/charminULTRA/Klipper-Input-Shaping-MK3S-Upgrade?tab=readme-ov-file.
As it sems no more maintained, I made my own one to correct some findings and respect some new Klipper possibilities as for instance native adaptive meshing without Kamp

I suggest to use the Mk3.5 Klipper Profiles like also described in the nice guide of charminULTRA above. As you can see there only less adaptions in the Prusaslicer Profiles are necessary
It´s not neccessary to remove in the Filamnet settings of Prusaslicer the custom Start-G-Code anymore as this config can interprete the Pressure Advance Settings there

Changes:
- New purgeline, no more in the middle of the prin bed
- Nozzle supports bed heating correctly
- adaptive meshing activated
- M572 macro added to interpret the PA values from the Prusaslicer Filament Settings
- Stealth Profile introduced (with this profile in Klipper and the Prusaslicer profiles for "structural" print we are still 50% faster then with a normal Mk3s+
- new organisation of the config files. Splitted in printer.cfg and a config folder with the rest of the files
