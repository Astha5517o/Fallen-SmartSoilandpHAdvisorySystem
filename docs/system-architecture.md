# System Architecture

**Document type:** Concept-level planning note, not a final circuit schematic.

## Planned signal flow

```text
Soil conditions
      |
      v
Capacitive soil-moisture sensor
      | analog signal (exact range TBD)
      v
Microcontroller / ADC (exact model TBD)
      |
      v
Readings + calibration + threshold logic
      |
      v
Local irrigation-status indicator
      |
      +---- later extension: Wi-Fi ----> phone status/alert
```

## Functional blocks

1. **Sensor:** produces an electrical output that changes with soil conditions.
2. **Controller:** samples the output using a compatible analog input.
3. **Calibration:** records readings for documented soil conditions; maps readings to a useful status only after testing.
4. **Status:** reports a cautious message such as “Check irrigation” rather than assuming one reading proves that watering is required.
5. **Wireless extension:** send data/status to a phone only after the basic system is stable.

## Electrical checks required before wiring

- Verify the sensor's supply-voltage range.
- Verify the sensor's maximum analog output under all expected conditions.
- Verify the selected controller's analog-input limits and ADC-capable pins.
- Confirm common ground and power requirements.
- Design any level shifting or signal conditioning from the verified specifications.
- Review the final schematic before applying power.

ESP32 GPIOs are not 5 V tolerant. Do not use this concept diagram as a pin-by-pin wiring guide.
