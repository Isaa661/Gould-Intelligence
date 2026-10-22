# Gould Intelligence

**Researching ways to make robot movements more accurate and reliable.**

Robots rely on software to decide how to move. Gould Intelligence is an independent research project exploring whether that software can be improved **without replacing the original system**. We test ideas, compare results, and report what works as well as what doesn't.

## What we've tested

### NVIDIA GR00T N1.7 — robot movement predictions

We ran NVIDIA's GR00T AI model on recordings of real robot movements and compared its joint-position predictions with the recorded actions.

In two recordings that had been set aside for evaluation, Gould's experimental predictions showed less error than the original GR00T predictions:

| Recording | Reduction in joint-position prediction error |
| --- | ---: |
| Test 1 (Episode 6) | **18.77%** |
| Test 2 (Episode 7) | **21.89%** |

The experiment was decided before looking at these two recordings. It involved **12 short prediction samples in total**, and NVIDIA's original model was left unchanged.

**What this means:** Gould's joint-position predictions matched the recorded data more closely in these small offline tests. **It does not yet mean a physical robot moved better, completed tasks more successfully, or became safer.** We have not demonstrated improvements to GR00T's gripper or end-effector movements.

### Unitree G1 — separate walking simulations

In earlier computer-simulation tests with a publicly available Unitree G1 walking controller, Gould reduced average movement-tracking error by around **6%** under some simulated disturbances.

These results came from simulations, **not tests on a physical humanoid robot**.

## What we're working on next

- Making predictions of arm and gripper movements more accurate.
- Testing whether improvements help robots complete tasks, not just match recorded data.
- Investigating whether the approach works with more than one type of robot controller.
- Keeping evaluations clear, reproducible and fair.

## Current status

Gould is a **research-stage prototype**, not a proven commercial or safety-certified robot system.

Gould Intelligence is independent and **not affiliated with or endorsed by NVIDIA or Unitree**.

For research enquiries, visit the project website.
