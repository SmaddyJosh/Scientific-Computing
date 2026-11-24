# BIT 2118 Scientific Computing - Group Work (Tasks A to S)

Mathematical analysis, program modification, interpretation and real-world cases.
Python programs for Tasks 2 to 20 of the BIT 2118 course, plus one modified
real-world case for every task. The written report is in `docs/`.

## Group members

| No. | Name | Registration number |
|-----|------|---------------------|
| 1 | Dickens Okoth | BSCCS/2024/53418 |
| 2 | Harrison Mutua | BSCCS/2024/54032 |
| 3 | Joseph Rai | BSCCS/2024/53718 |
| 4 | Felix Kariuki | BSCCS/2024/51882 |
| 5 | Hezron Karithi | BSCCS/2024/73578 |
| 6 | Margret Mumbi | BSCCS/2024/50177 |
| 7 | James Mwanzia | BSCCS/2024/74071 |
| 8 | Rooney Mugacha | BSCCS/2024/60056 |
| 9 | Brian Kiptui | BSCCS/2024/53968 |
| 10 | Joshua Muli | BSCCS/2024/73427 |

## Folder structure

```
bit2118-scientific-computing/
|-- code/
|   |-- Task_02_numpy_arrays.py            ... Task_20_monte_carlo.py   (one file per task)
|   `-- new_cases/
|       `-- case_A_...py                   ... case_S_...py             (one file per real-world case)
|-- docs/
|   `-- BIT2118_Group_Work_Tasks_A-S.docx  (full report: outputs, graphs, interpretation)
|-- .gitignore
|-- README.md
`-- requirements.txt
```

* `code/Task_NN_*.py` - the task program. Each file has a **base program** and a
  **changed parameter** section, as asked in the report.
* `code/new_cases/case_X_*.py` - the **modified real-world case** for that task.

## Setup

Python 3.10 or newer is recommended (NumPy 2.x is needed for `np.trapezoid`).

```bash
python -m venv .venv
.venv\Scripts\activate          # Windows
# source .venv/bin/activate     # macOS / Linux
pip install -r requirements.txt
```

## Running a program

```bash
python code/Task_08_iterative_methods.py
python code/new_cases/case_G_heated_rod.py
```

Programs that draw a graph open a Matplotlib window (`plt.show()`). To run
everything without windows, set the backend first:

```bash
set MPLBACKEND=Agg             # Windows (cmd)
export MPLBACKEND=Agg          # macOS / Linux
```

## Task index

| Letter | Task | Real-world case | Task file | Case file |
|--------|------|-----------------|-----------|-----------|
| A | 2: NumPy arrays | Greenhouse humidity monitoring | `Task_02_numpy_arrays.py` | `case_A_greenhouse_humidity.py` |
| B | 3: Vectorization | VAT on one million transactions | `Task_03_vectorization.py` | `case_B_vat_transactions.py` |
| C | 4: Floating-point errors | Summing money in banking | `Task_04_floating_point_errors.py` | `case_C_banking_sums.py` |
| D | 5: Matrix algebra | Rotating and scaling a floor plan | `Task_05_matrix_algebra.py` | `case_D_floor_plan_on_map.py` |
| E | 6: Linear systems | Two-loop electrical circuit | `Task_06_linear_systems.py` | `case_E_two_loop_circuit.py` |
| F | 7: Gaussian elimination and LU | Resistive network, repeated loads | `Task_07_lu_decomposition.py` | `case_F_resistive_network.py` |
| G | 8: Iterative methods | Temperature along a rod | `Task_08_iterative_methods.py` | `case_G_heated_rod.py` |
| H | 9: Eigenvalues | Office network node importance | `Task_09_eigenvalues.py` | `case_H_office_network.py` |
| I | 10: Bisection and fixed point | Business break-even points | `Task_10_bisection_fixed_point.py` | `case_I_break_even.py` |
| J | 11: Newton and secant | True interest rate of a loan | `Task_11_newton_secant.py` | `case_J_loan_interest_rate.py` |
| K | 12: Nonlinear equations | Overlapping cell-tower coverage | `Task_12_nonlinear_equations.py` | `case_K_cell_tower_coverage.py` |
| L | 13: Interpolation | Missing soil-moisture reading | `Task_13_interpolation.py` | `case_L_soil_moisture.py` |
| M | 14: Curve fitting | Product demand forecasting | `Task_14_curve_fitting.py` | `case_M_demand_forecasting.py` |
| N | 15: Numerical differentiation | Acceleration from velocity data | `Task_15_numerical_differentiation.py` | `case_N_acceleration_from_velocity.py` |
| O | 16: Numerical integration | Distance from speed readings | `Task_16_numerical_integration.py` | `case_O_distance_from_speed.py` |
| P | 17: Euler method | Logistic population growth | `Task_17_euler_method.py` | `case_P_logistic_growth.py` |
| Q | 18: SciPy ODE solver | SIR epidemic model | `Task_18_scipy_ode_solver.py` | `case_Q_sir_epidemic.py` |
| R | 19: Optimization | Minimum-cost vehicle fleet | `Task_19_optimization.py` | `case_R_vehicle_fleet.py` |
| S | 20: Monte Carlo | Server-cluster reliability | `Task_20_monte_carlo.py` | `case_S_server_cluster_reliability.py` |

## Notes

* Random programs use fixed seeds, so results repeat. Timing results (Tasks 3 and 7)
  change slightly from one computer to another.
* The task programs were rebuilt from the inputs and operations described in the
  report. Where the report does not list a dataset, an input that reproduces the
  reported outputs was used (Tasks 2, 7, 14 and 16).

## References

Burden, R. L., & Faires, J. D. (2011). *Numerical analysis* (9th ed.). Brooks/Cole.
Chapra, S. C., & Canale, R. P. (2015). *Numerical methods for engineers* (7th ed.). McGraw-Hill.
Goldberg, D. (1991). What every computer scientist should know about floating-point arithmetic. *ACM Computing Surveys, 23*(1), 5-48.
Harris, C. R., et al. (2020). Array programming with NumPy. *Nature, 585*, 357-362.
Hunter, J. D. (2007). Matplotlib: A 2D graphics environment. *Computing in Science & Engineering, 9*(3), 90-95.
Kermack, W. O., & McKendrick, A. G. (1927). A contribution to the mathematical theory of epidemics. *Proc. Royal Society A, 115*(772), 700-721.
Virtanen, P., et al. (2020). SciPy 1.0. *Nature Methods, 17*, 261-272.
