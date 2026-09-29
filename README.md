# Drone-Based Impact-Acoustic Inspection for Concrete Delamination

**Status:** Active development (September 2026)  
**Project type:** High school independent research / engineering project  
**Current focus:** Concrete delamination (浮き・剥離) detection, quantitative impact-acoustic analysis, and UAV deployment

## Overview

Japan's bridges, tunnels, and other concrete infrastructure are aging rapidly, while inspection still depends heavily on visual inspection and manual hammer sounding. This project explores whether impact-acoustic measurements can be made more quantitative, repeatable, and eventually deployable on a drone.

The current research scope is intentionally narrow: **detecting and localizing concrete delamination / 浮き** rather than attempting to identify every possible form of infrastructure deterioration.

The long-term goal is to develop a system that can:

1. generate a repeatable mechanical impact,
2. record and analyze the resulting acoustic response,
3. distinguish healthy concrete from delaminated regions,
4. map suspected defects spatially,
5. remain usable under drone rotor noise and motion,
6. and ultimately perform autonomous inspection on real structures.

## Why Delamination?

Delamination is a subsurface separation within concrete. It can develop before obvious surface failure and is one of the reasons inspectors use hammer sounding in addition to visual inspection.

The project therefore focuses on a practical question:

> **Can controlled impact-acoustic measurements quantitatively and repeatably detect and localize subsurface delamination in concrete?**

A later engineering question is:

> **Can the same measurement be automated on a UAV under realistic inspection conditions?**

## Current Experimental Method

The present ground-test method uses a small steel-ball impact and microphone recording.

A controlled impact excites the concrete, and the recorded acoustic response is analyzed in the frequency domain. Delaminated regions can respond differently from healthy regions because the subsurface separation changes the local mechanical vibration of the concrete.

### Demonstrated so far

- Controlled tests using a **10 mm steel ball** and a smartphone microphone
- Comparison of healthy and artificially delaminated tile specimens
- Useful spectral differences observed in approximately the **1–8 kHz** range
- Spatial measurements over a **5 × 5 grid**
- Defect location visualized as a 2D acoustic map

These results are an early proof of concept. They do **not yet establish field performance, universal detection accuracy, or defect depth estimation**.

## Current Engineering R&D

The next stage is to replace the manual impact with a compact, repeatable mechanism suitable for robotic deployment.

Impact concepts under consideration include:

- **Ball impact mechanism** — preserves continuity with the successful steel-ball baseline
- **Direct servo hammer** — mechanically simple, captive impactor
- **Geared servo hammer** — trades excess servo torque for higher hammer angular velocity in a compact package

A useful initial energy benchmark comes from the successful ball-drop tests. For a 10 g impactor dropped from 10 cm:

```
E = mgh ≈ 0.010 × 9.81 × 0.10 ≈ 9.8 mJ
```

The first actuator designs will therefore target roughly this order of impact energy, then experimentally evaluate whether higher or lower energy improves defect discrimination.

The optimization target is **not maximum impact strength**. It is the lowest controlled impact energy that produces a repeatable, high-SNR response containing useful information about delamination.

## Key Research Questions

### 1. Repeatability
Can the impact mechanism produce sufficiently consistent excitation across repeated trials?

### 2. Detection performance
How reliably can the acoustic response distinguish healthy concrete from known delamination?

### 3. Detection limits
How do delamination size, depth, and separation affect detectability?

### 4. Noise robustness
How strongly does UAV propeller noise reduce acoustic discrimination, and what combination of mechanical isolation, microphone placement, and signal processing can recover the signal?

### 5. Robotic deployment
Can a drone position the sensor/impactor consistently enough to reproduce ground-test performance?

## Why Impact Acoustics Instead of Only Infrared Thermography?

Infrared thermography (IRT) is a strong non-contact inspection method and is especially attractive for rapid drone-based screening. However, passive IRT depends on environmental thermal conditions such as solar heating, time of day, weather, moisture, emissivity, and defect depth.

Impact acoustics uses a **controlled mechanical excitation**, giving the inspection system more direct control over the measurement input.

This project does not assume that impact acoustics is universally better than IRT. A more realistic comparison is:

- **IRT:** fast, non-contact, excellent for large-area screening
- **Impact acoustics:** slower and mechanically harder, but potentially more controllable and complementary for targeted confirmation and characterization

A future comparison will test both approaches on specimens with known defect geometry.

## Development Roadmap

```
Ground proof of concept
        ↓
Repeatable impact mechanism
        ↓
Controlled validation across defect conditions
        ↓
Drone-noise robustness
        ↓
Existing-UAV integration
        ↓
Autonomous positioning and mapping
        ↓
Field validation against independently known defects
```

The immediate priority is **ground validation and impact-mechanism development**, not custom-drone construction.

## Current Limitations

The project is still at an early research stage. Current limitations include:

- small number of specimens
- artificial defect conditions
- limited defect sizes/depths tested
- manual impact generation
- limited repeatability characterization
- no blind validation yet
- no field-structure validation yet
- no completed UAV-mounted acoustic measurement yet
- rotor-noise mitigation still under development

These are treated as experimental targets rather than hidden weaknesses.

## Repository Structure

```
tunnel-inspection-drone/
├── docs/       # Research documentation
├── hardware/   # Mechanical and electrical design
├── firmware/   # Embedded / actuator control
├── analysis/   # Signal-processing and analysis scripts
├── data/       # Experimental measurements
└── media/      # Photos, videos, diagrams
```

## Project Direction

The project began with broader nonlinear-acoustic ideas for internal concrete damage. After early experiments and external feedback, the scope was narrowed to a more testable and deployable problem: **quantitative detection of concrete delamination using repeatable impact acoustics**.

The aim is to progress from a laboratory proof of concept to a validated robotic inspection system, while keeping each engineering step tied to a measurable research question.

## Acknowledgments

This project has benefited from discussions and guidance from researchers and engineers in acoustics, infrastructure inspection, machine learning, and UAV deployment.

## Notes

This repository is a working research log. Methods, hardware, and claims will continue to change as new experiments are completed.

---

**Repository:** https://github.com/ryotaroozawa1-coder/tunnel-inspection-drone
