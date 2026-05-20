# Social-Force-Model

**A Python implementation of the Helbing–Molnár Social Force Model for pedestrian dynamics, validated against real trajectory data, with Pygame visualization and force/direction analysis.**

A microscopic pedestrian-dynamics simulator: agents are point-mass particles under the combined action of a *driving force* (toward goal), *agent–agent repulsion*, and *wall repulsion*. The simulator ingests real pedestrian-trajectory CSV data, evolves the dynamics over time, renders the live trajectories with Pygame, and produces post-hoc analyses of per-agent forces and direction changes.

## What this project does

- **Input:** real pedestrian-trajectory CSV with columns `(Track_ID, X, Y, Vx, Vy, Speed, Image_File)`.
- **Per-timestep dynamics** for each agent `i`:
  - **Driving force** toward goal velocity (relaxation time `DRIVING_FORCE_TAU`).
  - **Social repulsion** from every other agent `j` — exponentially decaying with inter-agent distance.
  - **Wall/boundary repulsion** for static obstacles.
  - Newtonian integration of the resultant acceleration to update velocity and position.
- **Live visualization** with Pygame: trajectories rendered frame-by-frame.
- **Post-hoc analysis** with Matplotlib: average force magnitudes per agent, direction-change statistics, velocity profiles.

## Background

The Social Force Model (Helbing & Molnár, *Physical Review E*, 1995) treats pedestrian motion as a deterministic dynamical system with social-interaction forces analogous to physical ones. It remains one of the most cited microscopic models for crowd simulation, evacuation studies, and autonomous-navigation context modelling.

## What's in here

| File | Purpose |
|---|---|
| `Social_Force_Github.ipynb` | Main notebook — model implementation, simulation loop, Pygame rendering, Matplotlib analysis |
| `real_data.csv` | Pedestrian-trajectory data used as input |
| `Social_Force_Model.pptx` | Slide deck of early experiments and motivation |
| `requirements.txt` | Python dependencies |

## Running it

```bash
pip install -r requirements.txt
```

Then open `Social_Force_Github.ipynb` and run cells in order. Make sure `real_data.csv` is in the working directory, or update the path constant at the top of the notebook.

## Tunable parameters

A few constants control the qualitative regime of the simulation:

- `SCALE` — pixel-to-metre scaling for the Pygame canvas.
- `DRIVING_FORCE_TAU` — relaxation time toward goal velocity. Small τ = sharper steering, large τ = lazier convergence.
- Agent-repulsion amplitude `A` and decay length `B` — control how strongly and how far agents push each other.

Sweeping these illustrates different crowd regimes — free flow, spontaneous lane formation, jamming at bottlenecks.

## References

- Helbing, D. & Molnár, P. (1995). *Social force model for pedestrian dynamics.* Physical Review E, 51(5), 4282.

---

*Author: Muhammad Hanzala Iqbal.*
