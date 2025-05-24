# Teacher Scheduling Optimization using Simulated Annealing

This project implements a weekly teacher scheduling system using the **Simulated Annealing** (SA) algorithm. It ensures that each teacher receives at least one teaching slot, with a maximum of 12 shifts per week, and adheres to various scheduling constraints.

---

## 🚀 Features

- Assigns 45 teachers to 48 available teaching time slots (6 days × 8 shifts, excluding 1 break per day).
- Ensures every teacher receives **at least 1 slot per week**.
- Allows up to 12 shifts per teacher to avoid overload.
- Prevents scheduling on lunch break shifts.
- Uses SA to find a low-cost, optimized timetable.
- Visualizes schedules using heatmaps and color legends.

---

## 🧠 Algorithm: Simulated Annealing

**Simulated Annealing (SA)** is a probabilistic optimization technique inspired by the annealing process in metallurgy. It works by exploring neighboring solutions and probabilistically accepting worse solutions to escape local optima.

- **Energy (Cost) difference:**

\[
\Delta E = \text{cost}(\text{neighbor}) - \text{cost}(\text{current})
\]

- **Acceptance probability for worse solution:**

\[
P = e^{-\frac{\Delta E}{T}}
\]

  - \( \Delta E \) = increase in cost (positive if neighbor is worse)
  - \( T \) = current temperature (controls exploration)

- **Temperature cooling schedule:**

\[
T_{\text{new}} = \alpha \times T_{\text{old}}, \quad 0 < \alpha < 1
\]

- **Algorithm steps:**

  1. Initialize current solution and temperature \( T \).
  2. Generate neighbor solution.
  3. Compute \(\Delta E\).
  4. If \(\Delta E < 0\), accept neighbor (better solution).
  5. Else, accept neighbor with probability \(P = e^{-\Delta E / T}\).
  6. Update temperature \( T = \alpha \times T \).
  7. Repeat until stopping criteria met (e.g., \(T < T_{\min}\)).

---
