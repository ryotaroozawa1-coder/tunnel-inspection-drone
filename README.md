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
tunnel-inspection-drone/
├── docs/ # Research documentation
├── hardware/ # Circuit diagrams, mechanical design
├── firmware/ # Arduino code
├── analysis/ # Python analysis scripts
├── data/ # Measurement data (as collected)
└── media/ # Photos, videos of build

## Timeline

| Date | Milestone |
|------|-----------|
| May 2026 | Project conceived |
| June 2026 | Piezo → INRAS pivot (Sugimoto-sensei) |
| July 2026 | Enomoto Sr. consultation, drone approach refined |
| August 2026 | Damage scenario reframe (Matsuzaki-sensei), Isago-sensei consultation |

## Acknowledgments

- **Enomoto Kotaro** (International Drone Association) — Drone deployment mentorship
- **Prof. Sugimoto Tsuneyoshi** (Toin University Yokohama) — Nonlinear acoustics guidance  
- **Prof. Matsuzaki Hiroshi** (Tokyo Institute of Science) — Damage mechanism critique
- **Prof. Isago Nobuharu** (Tokyo Metropolitan University) — Tunnel engineering consultation

## References

Selected key references:
- Van Den Abeele et al. (2000). "Nonlinear Elastic Wave Spectroscopy Techniques."
- Jin, Y. & Shokouhi, P. (2017). "Impact-based nonlinear resonant acoustic spectroscopy for concrete damage assessment."
- Asakura, T. et al. (1991). "Deterioration of tunnel lining concrete."
- Asakura, T. & Kojima, Y. (2003). "Tunnel maintenance in Japan."

---

*This is a working research repository. Content and structure will evolve as the project progresses.*
