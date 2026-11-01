# Problem Statement and MVP Scope

## Project question

Can a simple capacitive soil-moisture sensing setup provide repeatable readings that help a grower decide when soil may need attention?

## Context

Manual checking is simple but depends on the person, location, and timing of each check. A sensor could provide a more consistent measurement, but its output must be interpreted and tested for the specific sensor and soil.

## Proposed approach

The initial concept is to use a capacitive soil-moisture sensor with a microcontroller. The system will collect readings, compare them with a threshold chosen through testing, and communicate a plain-language status. Wireless phone alerts are a later extension, not a requirement for proving the sensor measurement works.

## MVP acceptance criteria

The first version should:

- Read sensor output safely using the selected controller.
- Show or log raw readings.
- Explain how the threshold was chosen.
- Distinguish between measured data and inferred irrigation status.
- Include repeatable tests and note the soil, sensor placement, and conditions.
- Fail clearly when the sensor is disconnected or readings are implausible, if this can be implemented reliably.

## Out of scope for the first version

- Automatic pump or valve control.
- Claims of exact volumetric water content without a validated calibration method.
- Claims of water savings, crop-yield improvement, or field reliability before testing.
- Phone notifications before basic sensing and status logic work.

## Open questions

- Which exact sensor model and output-voltage range will be used?
- Which controller and analog input will be used?
- What soil type and plant context will the first tests use?
- How will dry, moist, and wetter reference conditions be defined?
- What is the safe and practical power arrangement?
