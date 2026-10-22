# Gould Intelligence

**Research and evaluation for more reliable learned robot controllers.**

Gould Intelligence is an independent robotics research project investigating whether existing controllers can be made more accurate and robust while retaining the original systems as comparison baselines.

## Research evidence — October 2026

### NVIDIA GR00T N1.7 · Offline evaluation

In an internal study using genuine DROID robot recordings and predictions from NVIDIA GR00T N1.7 3B, a Gould research candidate reduced **joint-position mean absolute prediction error** on two previously reserved evaluation recordings:

| Evaluation recording | Reduction in joint-position prediction MAE |
| --- | ---: |
| Episode 6 | **18.77%** |
| Episode 7 | **21.89%** |

The evaluated correction was selected before these two recordings were assessed. The original NVIDIA model weights were not changed. The evaluation comprised **12 prediction windows across two recordings**.

**Scope:** These are preliminary **offline prediction-accuracy** results. They do not establish improvements in physical robot task completion, safety, general robotics performance, or other GR00T action streams. Further independent testing is needed.

### Unitree G1 · Separate simulation research

Earlier internal closed-loop simulation experiments with a publicly released Unitree G1 walking controller reported approximately **6% lower mean tracking error** under selected synthetic disturbance conditions. These are simulation-only findings, separate from the GR00T evaluation, and are not evidence of performance on a physical robot.

## Research priorities

- Improve end-effector and gripper prediction accuracy using suitable evaluation data.
- Test whether offline results lead to better task outcomes in closed-loop environments.
- Study performance and generalisation across different controllers.
- Report baseline comparisons, limitations, and reproducibility clearly.

## Project status

**Research-stage prototype.** No customer deployment, independently validated physical-robot improvement, or certification for robot safety is claimed.

Gould Intelligence is independent and is **not affiliated with or endorsed by NVIDIA or Unitree**. Brand and model names identify third-party technologies used in research.

Contact details and information about potential evaluations are available on the project website.
