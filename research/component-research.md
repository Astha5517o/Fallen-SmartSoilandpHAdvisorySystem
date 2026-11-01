# Component Research

**Status:** Candidate research only. Do not treat a component as selected until its exact model and specifications are checked.

## Capacitive soil-moisture sensor

Why consider it: a capacitive sensor can estimate changes associated with soil moisture without relying on two exposed conductive probes in the same way as a basic resistive probe.

Before choosing a model, record:

- Manufacturer and exact model / product link
- Supply-voltage range
- Analog-output range and whether output can exceed the controller's input limit
- Connector and pin labels
- Probe dimensions and material
- Documentation and any calibration guidance
- Known limitations, cost, and availability

## Microcontroller

An ESP32-family controller is being considered because some variants provide analog inputs and Wi-Fi. The exact board or chip is **not confirmed**.

Before selecting it, record:

- Exact model and board revision
- ADC-capable pin(s) from the official pinout
- Permitted input voltage and ADC characteristics
- Supply and regulator requirements
- USB/programming method
- Whether the project rules require a custom PCB rather than a ready-made development board

**Important:** ESP32 GPIOs are not 5 V tolerant. Never assume a sensor's analog output is safe; check the exact datasheets and measure/condition the signal appropriately.

## Optional indicators

An LED with a correctly calculated series resistor could indicate status. A buzzer is optional and should be omitted from the first version unless it has a clear benefit. Confirm component ratings before wiring.

## Selection table

| Part | Exact model | Key specification to verify | Status |
|---|---|---|---|
| Moisture sensor | TBD | Supply and analog-output voltage | Research needed |
| Controller | TBD | ADC input limits, Wi-Fi, power | Research needed |
| LED | TBD / optional | Forward voltage and current | Not selected |
| Series resistor | TBD / optional | Value based on LED and controller | Not selected |
| Power source/regulator | TBD | Voltage, current, protection | Not selected |
| Connectors/wire | TBD | Fit and current rating | Not selected |

Fill in this table only after checking reliable manufacturer documentation.
