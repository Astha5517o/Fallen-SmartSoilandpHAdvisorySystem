# Smart Soil Moisture Monitoring & Irrigation Alert System 🌱

Hi! I'm Astha, a Class 11 student exploring AI, electronics and ideas that can solve real problems. This project is one of my attempts to turn an idea I cared about into something I can actually design, test and improve.

The idea is simple: **can we help a farmer understand when the soil may need water, instead of relying only on a fixed watering schedule?**

I'm still learning hardware, so this repository is my real project notebook: the research, rough drawings, decisions, mistakes, things I need to check, and progress as I go. I want to keep the original work here too, not hide it behind polished documentation.

> **Current stage:** concept + research + first hand-drawn workflow/circuit idea. I have not yet verified the circuit, built the hardware prototype, calibrated the sensor, or collected test results. I'll update this as I actually do the work.

## Why I started thinking about this

Plants can be affected when they receive too much or too little water. Farmers also have busy schedules, and weather and soil conditions can change. My first idea was to make a device that checks moisture near plant roots and sends a useful status to a farmer's phone.

I had written an earlier problem statement and research notes before starting this repository structure. Those originals are linked below so my initial thinking stays part of the project.

## My current idea

1. A capacitive soil-moisture sensor measures a signal related to the moisture in the soil.
2. An ESP32-based controller reads the sensor signal.
3. I test the readings in the soil I use and work out a threshold that makes sense for that setup.
4. The device shows a simple status, for example **Moisture may be low — check irrigation**.
5. Later, if the basic version works, I can explore sending the status to a phone over Wi-Fi.
6. Solar power is something I've drawn as a possible power option, but I still need to research the power requirements before deciding how to build it.

This is an idea and plan, not a claim that all these features work already.

## My first hand-drawn workflow

My notebook drawing connects the sensor, ESP32 controller, threshold comparison, irrigation status/alert, power supply, LED and buzzer. It also has a solar-power idea. I'm treating it as an early concept drawing; the actual connections still need checking before I wire anything.

- [Read the notes from my first workflow/circuit idea](docs/first-workflow-notes.md)
- [See the concept-level system architecture](docs/system-architecture.md)

**Important checks before wiring:** confirm the exact sensor model and its supply/output voltage, the exact ESP32 board and ADC pin, and the LED/buzzer connections. ESP32 GPIO inputs are not 5 V tolerant. This drawing is not a verified circuit yet.

## My original work (please keep these!)

These files are my earlier notes and uploads. They are part of how the project started.

- [Original problem statement](Fallen-Soil%20moisture%20sensor/doc/problem-statement.txt.txt)
- [Original research folder, including PDFs and Word files](Fallen-Soil%20moisture%20sensor/research/)
- [Original images folder](Fallen-Soil%20moisture%20sensor/images/)
- [Original project folder](Fallen-Soil%20moisture%20sensor/)

## Repository map

- `Fallen-Soil moisture sensor/` — my original uploaded documents, images and research. I am keeping these in place.
- `research/` — newer research notes and questions to investigate
- `docs/` — how I currently understand the system and its design
- `hardware/schematic/` — final circuit files after the connections are verified
- `hardware/pcb/` — PCB design files if/when needed
- `CAD/` — 3D or mechanical design files if needed
- `firmware/` — code for the controller when I start testing it
- `testing/` — calibration notes, observations, failures and results
- `progress/` — my own dated progress journal
- `BOM.csv` — parts list; exact models still need to be confirmed

## Progress so far

- [x] Original problem statement and research files uploaded
- [x] Started organising the repository without replacing the original folder
- [x] Drew an initial workflow/circuit concept in my notebook
- [ ] Confirm the exact sensor and ESP32 board
- [ ] Check safe voltage levels and pin assignments
- [ ] Finalise the parts list with real part numbers
- [ ] Make and review the actual schematic
- [ ] Design a PCB if required
- [ ] Build and test the first version
- [ ] Record calibration readings and what they mean
- [ ] Try a phone alert only after the basic reading works

## What I still need to figure out

- Which exact capacitive sensor should I use?
- Which ESP32 board or custom controller design makes sense for the project requirements?
- How will I power the sensor and controller safely? Is solar practical for my version?
- What threshold works for my soil, and how will I test it rather than guess?
- What does the project need to include for the hardware programme's requirements?

## How I'm documenting this

I'm going to keep the notes honest and beginner-friendly. If something is just an idea, I'll call it an idea. If a circuit doesn't work, I'll write that down too. If I make a mistake, it can be part of the learning instead of something I pretend never happened.

The earlier concept was recognised by INSPIRE-MANAK, according to my records. This current repository documents the new design and implementation work; that recognition does **not** mean this version has already been built or tested.

Thanks for checking out my project!
