# Teacher Scheduling Optimization using Simulated Annealing Algorithm

## 👤 Author

| Name            | Role              | LinkedIn                                      |
|-----------------|-------------------|-----------------------------------------------|
| Jason Emmanuel  | Data Scientist | [linkedin.com/in/jasoneml](https://www.linkedin.com/in/jasoneml/) |

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

## 📈 How It Works Together

- The SA algorithm starts with a random schedule.  
- It calculates the total cost based on the above formula.  
- It generates neighbor schedules by changing teacher assignments randomly.  
- Moves that reduce cost are accepted.  
- Moves that increase cost might be accepted based on probability related to temperature.  
- Temperature gradually decreases to reduce acceptance of worse solutions over time.  
- After iterations, the best found schedule minimizes the total cost and respects constraints as much as possible.

---

## Result

<table>
  <tr>
    <td style="width:80%; vertical-align: top;">
      <img src="https://github.com/user-attachments/assets/285dfd9a-1468-4668-8d3c-3c886d44885e" alt="Schedule Heatmap" style="width:100%; height: auto;"/>
    </td>
    <td style="width:20%; vertical-align: top; padding-left: 15px;">
      <img src="https://github.com/user-attachments/assets/eba74f9d-c8f4-48b3-847a-6ba29562b053" alt="Legend" style="width:100%; height: auto;"/>
    </td>
  </tr>
</table>

The final schedule is visualized as a heatmap, where:

- Rows represent shifts (time slots).
- Columns represent days of the week.
- Each cell shows the initials of the assigned teacher and their subject.
- Empty or break shifts are left blank.
- A color-coded legend matches teachers with their subjects for easy identification.

This visualization helps quickly identify teacher workloads, shift distribution, and adherence to constraints.

---

## 🛠️ Tools and Libraries Used

| Tool / Library        | Purpose                                                                                     |
|----------------------|---------------------------------------------------------------------------------------------|
| **NumPy**            | Efficient numerical operations and array handling for the schedule matrix.                  |
| **Random**           | Generating random schedules and neighbor solutions in the Simulated Annealing algorithm.   |
| **Copy**             | Deep copying schedule states to avoid unintended mutations when exploring neighbors.        |
| **Matplotlib**       | Creating heatmap visualizations of the final schedule for easy interpretation.              |
| **Seaborn**          | Enhancing heatmap style and annotations for clearer visualization of schedules.             |
| **Matplotlib Patches** | Custom legend creation to match teacher names and subjects with their corresponding colors. |

---


