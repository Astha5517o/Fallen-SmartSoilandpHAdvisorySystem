# Smart Soil Moisture Monitoring & Irrigation Alert System

A student hardware project exploring a practical way to monitor soil moisture and help a grower decide when irrigation may be needed.

> **Current status:** Concept and research stage. The physical prototype, circuit, firmware, calibration results, and field tests are not yet complete. This repository will document progress as the project develops.

## Problem

Checking soil moisture manually can be inconsistent, and watering decisions may be made without a measured reading. This project will explore whether a low-cost electronic sensor can provide a useful moisture reading and a clear irrigation-status alert.

## Planned first version (MVP)

1. Read a capacitive soil-moisture sensor with a microcontroller.
2. Record raw sensor readings from the selected soil and sensor.
3. Calibrate and test readings under documented soil conditions.
4. Display a simple status such as **Moisture OK** or **Check irrigation** using a verified threshold.
5. Explore sending the reading/status to a phone over Wi-Fi after the basic measurement works.

The threshold and sensor readings will need testing. The device will not claim an exact moisture percentage or water-saving result unless those claims are validated.

## How it is intended to work

`Soil → Capacitive moisture sensor → Microcontroller → Calibrated threshold → Status/alert → (later) Phone over Wi-Fi`

See [the system architecture notes](docs/system-architecture.md).

## Repository map

- `research/` — problem definition, component research, and references
- `docs/` — system architecture, design decisions, and project notes
- `hardware/` — schematic and PCB design files as they are created
- `firmware/` — microcontroller code as it is developed
- `testing/` — test plans, observations, and calibration results
- `BOM.csv` — planned parts list; confirm exact models and prices before ordering

Empty folders may not appear on GitHub until they contain a file.

## Current limitations and safety

- The exact sensor, controller, power arrangement, and pin assignments still need to be selected and verified.
- ESP32 GPIO inputs are **not 5 V tolerant**. Check the sensor's output voltage against the exact controller's limits before connecting it.
- The diagrams and notes in this repository are planning documents, not a verified wiring schematic.
- Do not connect or power unverified hardware. Ask a knowledgeable adult or mentor to review wiring and soldering.

## Progress checklist

- [x] Create project repository and initial documentation
- [ ] Compare candidate capacitive soil-moisture sensors
- [ ] Confirm microcontroller and safe voltage compatibility
- [ ] Finalise component list with verified part numbers
- [ ] Draw and review the actual circuit schematic
- [ ] Design PCB if required for the project
- [ ] Build the first prototype
- [ ] Record calibration and repeatability tests
- [ ] Implement basic status/alert firmware
- [ ] Test Wi-Fi/phone notification as a later feature
- [ ] Document results, failures, and next steps

## Background

The project idea builds on an earlier soil-monitoring concept recognised by INSPIRE-MANAK, according to the project author's account. This repository documents the new design and implementation work; recognition of the earlier concept does not mean that this prototype has already been built or tested.

## Contributions and project integrity

Design decisions, test results, photos, and progress notes should reflect work actually completed. Update this README as the design changes, and label plans separately from verified results.
