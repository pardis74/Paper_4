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
