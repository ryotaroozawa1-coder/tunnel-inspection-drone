# Low-Cost Nonlinear Acoustic Inspection System for Aging Concrete Infrastructure

**Status:** Active development (Aug 2026 — Sept 2026)  
**Project type:** High school independent research  
**Target competition:** JSEC 2026 (submission Sept 29, 2026)

## Problem

Japan's tunnels, bridges, and other concrete infrastructure are aging simultaneously. By 2040, over 50% of Japan's tunnels will exceed 50 years of service. National law requires periodic inspection every 5 years, but many municipalities cannot comply — approximately 1 in 4 lacks any civil engineering staff, and traditional inspection equipment costs millions of yen. 

This project develops a low-cost drone-based system to detect internal microcracking in concrete structures using nonlinear acoustic parameters — bringing sophisticated NDT capability within reach of budget-constrained infrastructure operators.

## Technical Approach

The system uses **Impact-based Nonlinear Resonant Acoustic Spectroscopy (INRAS)** to measure two damage indicators:
- **α_f:** frequency-amplitude dependence parameter
- **ν:** slow dynamics recovery time constant

Both indicators are theoretically linked through Preisach-Mayergoyz space theory and sensitive to distributed internal microcracking that traditional visual inspection cannot detect.

**Hardware stack (~¥10,000 total):**
- Solenoid impactor for repeatable mechanical excitation
- Piezoelectric vibration sensor for signal detection
- Load cell + HX711 amplifier for impact force measurement
- Arduino Nano for control and data logging
- Autonomous drone platform (integration phase)

## Novelty Positioning

This project's contribution is engineering integration, not fundamental physics discovery:
1. Reducing INRAS equipment cost from ~¥10M to ~¥10K
2. Integrating measurement with autonomous drone deployment
3. Developing signal processing to separate concrete resonance from drone motor noise

The underlying physics is established in prior work (Jin & Shokouhi 2017, Van Den Abeele 2000). This work makes it accessible.

## Current Status (August 2026)

- Detection chain validated on metal bowl and concrete block (tuning fork tests)
- Physics understanding developed through consultation with Prof. Sugimoto (Toin University) and Prof. Matsuzaki (Tokyo Institute of Science)
- Hardware ordered, delivery expected Aug 11-19
- Bench setup construction begins mid-August
- Drone integration planned with International Drone Association mentorship (August internship confirmed)

## Repository Structure
