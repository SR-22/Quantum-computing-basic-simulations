# **Bell State Generation (Entanglement)**

This mini-project implements all four Bell states using **Qiskit**, visualizes them using **statevectors** and **Bloch spheres**, and verifies their purity to confirm they are maximally entangled states.

This project is part of my collection of beginner-friendly quantum computing implementations, showcasing foundational concepts in quantum information.

---

## ⭐ **Project Summary**

Bell states are the simplest and most widely used examples of **quantum entanglement**.
In this project, I:

* Construct all four Bell states:
  **|Φ⁺⟩, |Φ⁻⟩, |Ψ⁺⟩, |Ψ⁻⟩**
* Build the corresponding **quantum circuits** using Qiskit
* Generate **statevectors** and render them in **LaTeX**
* Visualize states on the **Bloch sphere**
* Compute **purity** using Qiskit to verify maximal entanglement

This project uses **only Qiskit Aer simulators** (no IBM Quantum hardware required).

---

## 📂 **Repository Structure**

```
bell-states/
│
├── Bell's State.ipynb           # Full Jupyter Notebook with circuits, visualizations, and purity checks
├── Readme.md                  # Explanation 

```

---

## 🧪 **What You’ll Learn**

This project demonstrates:

* How to prepare entangled quantum states
* Use of `H`, `CX`, `X`, and `Z` gates to generate each Bell state
* Extracting `Statevector` and LaTeX representation
* Visualizing qubit states with Bloch spheres
* Checking whether a state is pure or mixed
* Basic quantum circuit design using Qiskit

---

## 🔧 **How to Run**

1. Install dependencies:

```bash
pip install qiskit matplotlib
```

2. Open the notebook:

```bash
jupyter notebook BellStates.ipynb
```

3. Run all cells to generate:

* Circuit diagrams
* Bell state LaTeX outputs
* Bloch sphere visualizations
* Purity values

---

## 📘 **Example Output**

| Bell State | Definition                   |
| ---------- | ----------  -----  --------- |
| **Φ⁺**     | (|00⟩ + |11⟩) / √2 |
| **Φ⁻**     | (|00⟩ − |11⟩) / √2 |
| **Ψ⁺**     | (|01⟩ + |10⟩) / √2 |
| **Ψ⁻**     | (|01⟩ − |10⟩) / √2 |

Circuit example (Φ⁺):

* Apply **H** to qubit 0
* Apply **CX** from qubit 0 → 1

---

## 🎯 **Why This Project Is Useful**

* Shows understanding of **quantum entanglement**, a core concept for quantum communication and algorithms
* Demonstrates hands-on experience with **Qiskit**, a leading quantum SDK
* Includes both **practical implementation** and **optional advanced theory**
* Good entry-level project for roles in QC, quantum software, or research internships

---

## 📚 **References**

* Qiskit Textbook — *Quantum Information*
* M. Nielsen & I. Chuang — *Quantum Computation and Quantum Information*
* IBM Quantum Documentation

