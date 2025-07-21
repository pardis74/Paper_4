# Whale Optimization Algorithm for Capacitated Hub Location Problem

This repository contains a Python implementation of the Whale Optimization Algorithm (WOA) to solve the Capacitated Hub Location Problem (CHLP) in computer networks, with a focus on mitigating disruptions. The model aims to minimize both information transfer time and the cost of establishing and maintaining hubs, including considerations for backup hubs and potential failures.

This implementation is based on the research paper:  
**"Whale Optimization Algorithm for Solving the Capacitated Hub Location Problem in Computer Networks Considering Disruptions"**  
by Anita Ershadi Oskouei, Ali Vaziri, and Pardis Sadatian Moghaddam.

---

## Features

- **Bi-objective Optimization**  
  Minimizes two conflicting objectives:  
  - Z1: Total Information Transfer Time  
  - Z2: Total Network Cost

- **Capacitated Hubs**  
  Each hub has a defined capacity for data transfer.

- **Disruption Consideration**  
  Models hub failures and the role of backup hubs in maintaining network availability.

- **Constraint Handling**  
  Uses penalty functions to enforce operational constraints such as node-to-hub assignments, hub connectivity, capacity limits, and failure conditions.

- **Whale Optimization Algorithm**  
  A metaheuristic algorithm to find near-optimal solutions for this NP-hard problem.

- **Synthetic Data Generation**  
  Built-in data generation for parameters, allowing the code to run without external datasets.

- **Fitness History Plotting**  
  Visualizes the optimization process by plotting the best fitness value over iterations.

---

## Problem Formulation (Simplified)

The problem involves selecting optimal hub locations, assigning nodes to hubs, determining inter-hub connections, and managing hub failures and backup assignments over multiple time periods. The objective is to minimize a weighted sum of time and cost, subject to constraints on capacity, connectivity, and operational logic.

---

## Installation

Make sure you have Python installed. Then install the required libraries:

```bash
pip install numpy matplotlib


Customizing Parameters
Edit the following parameters in woa_hub_location.py to customize the problem and algorithm:

python
Copy
Edit
# Problem Parameters
NUM_HUBS = 5
NUM_NODES = 10
NUM_BACKUP_HUBS = 3
NUM_TIME_PERIODS = 3

# Capacities, times, and costs can be adjusted as needed
# For example:
# HUB_CAPACITIES = np.array([700, 800, 750, 900, 850])

# WOA Parameters
POPULATION_SIZE = 50
MAX_ITERATIONS = 100
WEIGHT_Z1 = 0.5  # prioritize information transfer time
WEIGHT_Z2 = 0.5  # prioritize network cost
M = 1000000      # penalty constant
Adjust WEIGHT_Z1 and WEIGHT_Z2 to explore trade-offs between transfer time and cost. For example, WEIGHT_Z1 = 0.8 and WEIGHT_Z2 = 0.2 prioritizes minimizing transfer time.

Output
The script outputs:

Optimization progress per iteration (best fitness, Z1, Z2)

Final best fitness and corresponding Z1 and Z2 values

Optimal decision variables as NumPy arrays:

x_it: Hub establishment status (binary)

x_lit: Backup hub assignment (binary)

u_it: Hub failure status (binary)

y_ikt: Node-hub assignment (binary)

w_ijt: Hub-hub connectivity (binary)

z_ik: Node-hub data transfer volume (derived)

v_ij: Hub-hub data transfer volume (derived)

A plot of fitness history over iterations

Future Improvements
Replace synthetic data with real-world datasets

Implement advanced constraint handling techniques

Perform parameter tuning and sensitivity analysis for WOA

Compare WOA with other metaheuristics such as Genetic Algorithms or Particle Swarm Optimization

Improve scalability for larger problem instances

Model more complex dynamic disruptions and demand changes

Feel free to open issues or contribute to the project!

vbnet
Copy
Edit

Let me know if you'd like it adjusted or shortened!








Ask ChatGPT
