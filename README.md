# Gould Intelligence

**Researching ways to make robot movements more accurate and reliable.**

Gould Intelligence is an independent robotics research project investigating corrections to existing robotics AI models and controllers. Our experiments compare modified behaviour with the original system, retain original model weights and disclose limitations as well as improvements.

Website: https://isaa661.github.io/Gould-Intelligence/

## Latest results — October 2026

### NVIDIA GR00T N1.7 — end-effector predictions

In an independent offline evaluation on **six previously unused recorded episodes** and **24 short prediction windows**, Gould Intelligence's frozen experimental correction produced:

| Metric | Reduction in prediction error |
| --- | ---: |
| Overall end-effector prediction error | **5.10%** |
| Position-only error (XYZ) | **0.81%** |
| Position-only error during commanded motion | **0.05%** |

The overall error reduction does **not** demonstrate better physical robot task success or meaningful improvement in position error during motion. NVIDIA model weights were unmodified.

### Unitree G1 and H1 — separate closed-loop walking simulations

In **12-second MuJoCo stress simulations** featuring changing speed commands and simulated disturbances, frozen experimental controller-specific corrections achieved the following results versus the unchanged original policies:

| Robot/controller | Speed-tracking error reduction | Scenarios improved |
| --- | ---: | ---: |
| Unitree G1 12DoF walking policy | **20.77%** | **7 / 7** |
| Unitree H1 walking policy | **12.68%** | **7 / 7** |

Both baseline and corrected controllers remained stable during these trials, with **no additional simulated falls**. The separately tested H1-2 policy remained on exact fallback after its candidate failed the required checks.

These are limited **simulation-only speed-tracking results**, not a demonstration of improved walking on real robots, safer operation or completed physical tasks. Original Unitree controller weights were unchanged.

## Earlier experiments — separate research

- **GR00T joint-position predictions:** Two earlier offline test recordings with 12 short prediction samples combined reported **18.77%** and **21.89%** lower joint-position prediction error. These results use a different metric from the newer end-effector evaluation.
- **Original Gould Intelligence Unitree G1 research:** Earlier simulation experiments reported approximately **6.3%** lower average movement-tracking error under selected simulated disturbances. This historic system is separate from the newer G1 controller correction.

## Status and next steps

Gould Intelligence remains a **research-stage prototype**, not a safety-certified robot system or a commercially validated product. Next steps include validating real task outcomes, broader independent simulation and robot evaluation, and integrating our experimental research modules into an audited installable sidecar.

Gould Intelligence is independent and **not affiliated with or endorsed by NVIDIA or Unitree**. Private correction methods and internal research code are not published here.

For research enquiries, see the website.
