# PCB design

I made the first PCB layout in EasyEDA from my schematic. I also checked its 3D view to see how the main modules may fit on the board.

## Current files

- `PCB_PCB_Smart-soil-and-ai-ph-advisory-system_2_2026-11-21 (1).png` — current PCB layout image

## Status

This is a design preview, not a fabrication-ready PCB yet. The ESP32 development board has not arrived, and the schematic still needs electrical and footprint checks. The 3D view is useful for checking placement, but it does not prove that the circuit will work.

## Before fabrication

1. Match the ESP32 footprint to the exact board that arrives.
2. Check the moisture sensor, pH module, DS18B20 and OLED connector pin orders.
3. Correct the GPIO mapping and DS18B20 pull-up resistor in the schematic.
4. Finalize the pH interface and safe analog signal range.
5. Design the solar charging and regulated power input as a separate verified power stage, or use a suitable external power module.
6. Update the PCB from the corrected schematic.
7. Run ERC and DRC and fix all errors.
8. Check board outline, mounting holes, USB access, connector clearance and component orientation.
9. Inspect the 3D view again and export the EasyEDA source files and Gerbers.

I will only call the PCB ready for fabrication after these checks are complete.
