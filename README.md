# General_Physics

# Dynamics of a Falling Rigid Rod: Simulation & Verification

This repository contains a Python-based numerical simulation that models the plane motion of a uniform thin rigid rod released from rest on various horizontal surfaces. The simulation is based on the theoretical framework and experimental setups described in the *American Journal of Physics* (AJP) paper: **"Experiments with a falling rod" by Vitor Oliveira (2016)**.

## Physics Background

When a uniform rigid rod of mass $M$ and length $L$ is released from an initial angle $\theta_0$, its center of mass undergoes both rotational and translational accelerations. Depending on the static friction coefficient ($\mu_s$) and the release angle, the bottom end of the rod exhibits distinct behavioral regimes:

1. **Non-Slipping Regime:** The bottom end remains strictly at rest. The critical angle where the required frictional force vanishes is given by $\theta_c = \sin^{-1}(\frac{2}{3}\sin\theta_0)$.
2. **Slipping Regime:** If the required frictional force exceeds the maximum static friction ($|f| > \mu_s N$), the bottom end begins to slide. 
   - **Backward Slip:** Occurs at larger angles for surfaces with small friction coefficients.
   - **Forward Slip:** Occurs for surfaces with high friction coefficients or intermediate values depending on $\theta_0$.

This simulation solves the non-linear differential equations of motion using the **Euler method** to numerically simulate relationship between the falling angle ($\theta$) and the base displacement ($x_b$).

---

## Features

- **Multi-Surface Comparison:** Simulates three distinct physical surface textures:
  - **cloth** ($\mu_s = 1.9$, $\mu_k = 0.8$)
  - **marble** ($\mu_s = 0.9$, $\mu_k = 0.33$)
  - **steel** ($\mu_s = 0.27$, $\mu_k = 0.185$)
- **Multi-Angle Analysis:** Evaluates three initial release angles ($75^\circ$, $26^\circ$, and $5.6^\circ$) simultaneously on each canvas.
- **High-Resolution Discrete Tracking:** Captures state transitions at a discrete time step of $\Delta t = 0.005\text{ s}$.
- **Advanced Visualization:** Plots continuous trajectories coupled with hollow circle markers (`facecolors='none'`) to visualize kinematic density (velocity/acceleration changes) seamlessly.

---

## Prerequisites

Ensure you have the following Python libraries installed before running the script:

```bash
pip install numpy matplotlib pandas
