# Physical Design Automation (PDA) Algorithms

This repository contains my implementations for the **Physical Design Automation** course, focusing on the core algorithms of the VLSI physical design flow. The projects range from netlist partitioning to advanced analog placement and standard cell legalization.

---

## 🚀 Overview

The goal of this project series is to solve complex optimization problems in chip design using efficient data structures and heuristic algorithms. Key areas include:
* **Partitioning**: Min-cut algorithms for multi-die design.
* **Floorplanning**: Slicing tree and Simulated Annealing.
* **Placement**: Analog placement with symmetry constraints.
* **Legalization**: Row-based movement optimization.

---

## 📂 Homework Modules

### HW1: EDA Tool Environment
* **Objective**: Familiarization with industrial EDA toolchains, design formats, and the physical design environment.

### HW2: Two-Way Min-Cut Partitioning
* **Problem**: Given a set of cells $C$ and nets $N$, partition cells into two disjoint groups $A$ and $B$ (representing different dies) to minimize the **cut size**.
* **Key Features**:
    * Implemented **Fiduccia-Mattheyses (FM) Algorithm** (or your specific heuristic).
    * Optimized gain-cell data structures for efficient cell movement and gain updates.
    * Handles net weights to minimize the total cost of nets spanning both partitions.

### HW3: Fixed-Outline Slicing Floorplan
* **Reference**: *“A New Algorithm for Floorplan Design”* by Wong and Liu (DAC 1986).
* **Objective**: Solve the fixed-outline floorplanning problem with hard blocks.
* **Key Features**:
    * **Polish Expression** & **Slicing Tree** representation.
    * **Simulated Annealing (SA)** engine to optimize area and wirelength under fixed-outline constraints.
    * Implemented Wong-Liu's normalized Polish expression moves to explore the solution space.

### HW4: Analog Placement with Symmetry Constraints
* **Reference**: *“Analog Placement Based on Symmetry-Island Formulation”* by Lin et al. (TCAD 2009).
* **Objective**: Automate the placement of analog devices while strictly adhering to symmetry group constraints to maintain circuit performance.
* **Key Features**:
    * Implementation of **Symmetry-Island** formulation.
    * Balanced placement density with strict matching requirements for analog sensitivity.
    * Validated using standard IEEE TCAD benchmark circuits.

### HW5: Standard Cell Legalization (Abacus)
* **Reference**: *“Abacus: Fast Legalization of Standard Cell Circuits with Minimal Movement”* by Spindler et al. (ISPD 2008).
* **Objective**: Legalize a global placement result into standard cell rows while minimizing the **Total Euclidean Displacement**.
* **Key Features**:
    * **Abacus Algorithm**: A high-efficiency row-based legalization technique.
    * Cluster-based movement strategy to ensure minimal deviation from the optimized global placement positions.
    * Ensures all cells are aligned to row sites without overlaps.

---

## 🛠️ Development Environment
* **Language**: C++ (C++11/14/17)
* **Build System**: Makefile / CMake
* **Operating System**: Linux (Ubuntu / RHEL)

## 📊 Performance
| Module | Key Algorithm | Primary Metric |
| :--- | :--- | :--- |
| HW2 | FM Algorithm | Cut Size |
| HW3 | Simulated Annealing | Area / Wirelength |
| HW4 | Symmetry-Island | Displacement / Symmetry |
| HW5 | Abacus | Total Displacement |

---

## 📧 Contact
For any questions regarding the implementations, feel free to open an issue or contact me via GitHub.
