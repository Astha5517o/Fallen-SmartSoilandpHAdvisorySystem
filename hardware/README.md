# Hardware

This folder contains the circuit and PCB work for SMART SOIL.

I am making this as a small soil-monitoring device using an ESP32. The first version is planned to read soil moisture and temperature, and the pH section is being added with an external pH interface module. The ESP32 will send readings to a phone using Bluetooth Low Energy (BLE).

## Main parts

- ESP32-WROOM-32 development board
- Capacitive soil moisture sensor
- DS18B20 waterproof temperature probe
- Analog pH interface module and pH probe (still to be selected and tested)
- 0.96 inch SSD1306 I2C OLED display
- LEDs and an active buzzer for local status alerts
- Solar panel and 18650 battery system (power-management module still required)

The complete component list is in [BOM.csv](BOM.csv).

## Current design status

- [Schematic files](schematic/README.md) have been exported from EasyEDA.
- [PCB files and render](Pcb/README.md) are being prepared.
- The current PCB is a design preview. It has not been electrically validated or manufactured yet.
- The ESP32 board is still awaiting delivery, so the exact board dimensions, connector and footprint must be checked against the real board before fabrication.
- The pH interface and solar charging/power-management circuit are not yet finalized.

## Important checks before ordering a PCB

1. Confirm that the ESP32 symbol and footprint match the exact 30-pin development board that arrives.
2. Use GPIO34 for the moisture analog input and GPIO35 for the pH analog input only after confirming the pH module output is within the ESP32 input range.
3. GPIO34 and GPIO35 are input-only pins. They must not be used to drive LEDs or a buzzer.
4. Give the DS18B20 data line a 4.7k ohm pull-up resistor to 3.3V.
5. Check that no two functions share the same GPIO by mistake. The current schematic needs a final pin-conflict review.
6. Do not connect the 6V solar panel or 18650 cell directly to the ESP32. A suitable solar charging, battery-protection and regulated power module is still needed.
7. Run EasyEDA ERC and PCB DRC, then inspect the 3D model and connector positions.

This is still a design-stage project. I will update this folder after the physical prototype is tested.
