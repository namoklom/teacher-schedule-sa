# Teacher Scheduling Optimization using Simulated Annealing

This project implements a weekly teacher scheduling system using the **Simulated Annealing** (SA) algorithm. It ensures that each teacher receives at least one teaching slot, with a maximum of 12 shifts per week, and adheres to various scheduling constraints.

**Simulated Annealing (SA)** is a probabilistic optimization algorithm inspired by the physical process of annealing in metallurgy, where metals are heated and then slowly cooled to remove defects and reach a more stable, low-energy state.

---

## 📅 Constraints and Cost Formulas in Teacher Scheduling

### Let:

<img width="600" alt="image" src="https://github.com/user-attachments/assets/d758932c-b8a3-406a-959c-44185e002452" />

### 1. Break Shift Must Be Empty

<img width="650" alt="image" src="https://github.com/user-attachments/assets/d5882f36-33b4-4e3e-bb93-4f9fff10a3e0" />

### 2. No Teacher Teaches More Than One Shift per Day

<img width="600" alt="image" src="https://github.com/user-attachments/assets/1ba46746-5b73-4215-bcd0-2c92bf4f2412" />

### 3. Maximum Number of Shifts per Teacher per Week (12 shifts)

<img width="600" alt="image" src="https://github.com/user-attachments/assets/0807cd47-f628-4a2c-9a6c-05b8f822f895" />

### 4. Every Teacher Must Teach at Least One Shift per Week

<img width="600" alt="image" src="https://github.com/user-attachments/assets/4175048a-babb-4266-85c9-0261787bb8df" />

### Total Cost Function

<img width="600" alt="image" src="https://github.com/user-attachments/assets/ecf282c4-a168-4c07-ab4f-b69f439dd5a6" />

---



