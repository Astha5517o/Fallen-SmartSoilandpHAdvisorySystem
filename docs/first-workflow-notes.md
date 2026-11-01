# My first workflow and circuit idea — 1 November 2026

This note describes what I drew in my notebook today. The drawing is a first concept, not a verified circuit.

## What I drew

### Workflow
- A capacitive soil-moisture sensor is placed in soil near the plant roots.
- The sensor signal goes to an ESP32 controller.
- The controller compares the reading with a threshold.
- The result becomes a simple status: moisture sufficient, or irrigation may be needed.
- An alert is shown/sent.
- I drew solar power as a possible power source.

### Rough circuit ideas
I also sketched a sensor connection labelled VCC, GND and AOUT; an ESP32 ADC input; a power-supply block; common ground; and optional output parts: an LED with a resistor and a buzzer.

## Things I need to verify before wiring

1. Exact capacitive sensor model and its recommended supply voltage.
2. The sensor's output range and whether it is safe for the chosen ESP32 ADC input.
3. Exact ESP32 board/module and a suitable ADC pin.
4. Correct LED resistor value and buzzer voltage/current requirements.
5. A safe power arrangement; the solar option needs its own power-budget research.
6. Whether the hardware programme expects a custom PCB rather than a ready-made development board.

**Safety note:** ESP32 GPIO inputs are not 5 V tolerant. Do not connect parts based only on this sketch. Verify datasheets and have a knowledgeable mentor/adult review the final schematic before powering it.

## What is not done yet

- This is not a finished schematic.
- The components and pin assignments are not final.
- I have not recorded physical test results in this note.
- Phone notifications and solar power remain planned options until I verify the basic design.
