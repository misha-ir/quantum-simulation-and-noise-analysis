# Quantum Simulation and Noise Analysis

Exploration of quantum simulation techniques, focusing on Hamiltonian evolution, Trotterization methods, and variational quantum algorithms, with detailed analysis of noise effects on quantum circuits.

## Project Overview

This project examines quantum simulation from foundational single-qubit dynamics to multi-qubit variational algorithms, progressively introducing complexity and realistic noise models. The work is organized into three distinct phases, each building upon the previous one.

## Phase Descriptions

### Phase 1 — Single-Qubit Rabi Oscillations
Explores the fundamental behavior of a single qubit under a time-varying Hamiltonian. Demonstrates Rabi oscillations by comparing three approaches:
- Analytical solution using the time-evolution operator
- Numerical simulation with matrix exponentiation
- Qiskit circuit implementation using Rx gates

**Key Concepts:** Hamiltonian dynamics, time evolution, Bloch sphere rotations, quantum gates

### Phase 2 — Two-Qubit Ising Hamiltonian and Trotterization
Extends to two-qubit systems with interactions, focusing on the Ising model Hamiltonian. Examines how to approximate continuous-time evolution using discrete quantum gates through Trotterization.

**Key Topics:**
- Exact vs. approximate time evolution
- First-order and second-order Trotter decompositions
- Trade-offs between circuit depth and accuracy
- Impact of gate noise, decoherence, and measurement errors

### Phase 3 — VQE for the Heisenberg Spin Chain
Implements the Variational Quantum Eigensolver (VQE) algorithm to find the ground-state energy of a 4-qubit Heisenberg spin chain.

**Key Components:**
- Parameterized ansatz circuits with varying depths
- Classical optimization (COBYLA) for parameter tuning
- Comparison of ideal vs. noisy simulations
- Hardware experiments on IBM quantum devices
- Analysis of VQE variance and optimization challenges under noise

## File Structure

### Notebooks
- **`phase_one.ipynb`** — Single-qubit Rabi oscillations, time evolution, and gate implementations
- **`phase_two.ipynb`** — Two-qubit Ising model, Trotterization, and noise analysis
- **`phase_three.ipynb`** — VQE implementation, optimization, and hardware experiments

### Theory Documents
- **`phase1_theory.pdf`** — Theoretical background for Phase 1
- **`phase2_theory.pdf`** — Theoretical background for Phase 2
- **`phase3_theory.pdf`** — Theoretical background for Phase 3

### Results & Visualizations
- **`figures/`** — Directory containing all generated plots and circuit diagrams
  - `figures/p1/` — Phase 1 visualizations (Rabi oscillations)
  - `figures/p2/` — Phase 2 visualizations (Trotter circuits, error analysis, noise comparisons)
  - `figures/p3/` — Phase 3 visualizations (VQE convergence, depth comparisons, hardware results)

### Data Files
- **`phase3_hardware_results_ibm_fez_depth2_shots1000_Nevals3.npz`** — Hardware experiment data from IBM Fez backend

### Documentation
- **`final_report.pdf`** — Comprehensive project report with detailed analysis and findings

## Dependencies

The project uses the following Python libraries:
- **Qiskit** — Quantum computing framework (circuits, simulation, hardware access)
- **Qiskit Aer** — High-performance quantum circuit simulators with noise models
- **Qiskit IBM Runtime** — Access to IBM Quantum hardware and fake backends
- **NumPy** — Numerical computing
- **SciPy** — Scientific computing (matrix exponentiation, optimization)
- **Matplotlib** — Plotting and visualization

## Getting Started

1. **Install dependencies:**
   ```bash
   pip install qiskit qiskit-aer qiskit-ibm-runtime numpy scipy matplotlib
   ```

2. **Run the notebooks in order:**
   - Start with `phase_one.ipynb` for foundational concepts
   - Progress to `phase_two.ipynb` for multi-qubit systems
   - Complete with `phase_three.ipynb` for VQE and hardware experiments

3. **IBM Quantum Access (Optional):**
   - For Phase 3 hardware experiments, you'll need an IBM Quantum account
   - Configure your API credentials using `QiskitRuntimeService`
