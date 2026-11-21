# Schematic

I used EasyEDA to draw the first circuit for SMART SOIL. The exported PDF and SVG are included in this folder.

## Files

- `Schematic_Smart-soil-and-ai-ph-advisory-system_2026-11-15.pdf` — exported schematic PDF
- `Schematic_Smart-soil-and-ai-ph-advisory-system_2026-11-15.svg` — schematic image in SVG format

The schematic is an evolving design, not a tested circuit yet. The latest changes may be newer than these exported files, so I will replace the exports after the next verified update.

## Planned signal connections

| Function | Planned ESP32 connection |
|---|---|
| Soil moisture analog output | GPIO34 / ADC1 |
| pH interface analog output | GPIO35 / ADC1, after checking output voltage |
| OLED SDA | GPIO21 |
| OLED SCL | GPIO22 |
| DS18B20 data | GPIO32, with 4.7k ohm pull-up to 3.3V |
| Buzzer control | GPIO26 |
| Status LEDs | GPIO25, GPIO27 and GPIO33 |

These are the intended connections for the next schematic revision. They are not a claim that the current exported schematic already has this exact mapping.

## Changes to make before PCB fabrication

- Replace the 1k resistor on the DS18B20 data line with a 4.7k ohm pull-up resistor.
- Keep GPIO34 and GPIO35 for analog sensor inputs; they are input-only.
- Move LED and buzzer control signals to output-capable GPIO pins.
- Check that the buzzer control pin and temperature data pin are not accidentally connected to the same GPIO.
- Confirm the pH interface output never exceeds the ESP32 ADC input limit. Add suitable signal conditioning if the selected module needs it.
- Confirm the OLED connector pin order from the actual display module.
- Confirm all power and ground connections and check for unconnected pins using ERC.

The AI features are part of the phone app/software plan. An AI symbol is not needed in the electrical schematic because AI processing does not happen as a separate electronic component on this board.
