# Grover’s Algorithm 

This repository contains a complete implementation of **Grover’s Search Algorithm** using **Qiskit Aer**.
The notebook demonstrates how quantum amplitude amplification can be used to find a marked element in an unstructured database in **O(√N)** time — a quadratic speed-up compared to classical search.

---

## 🚀 Project Overview

Grover’s algorithm solves the following problem:

> Given an unstructured database of size **N**, find the single marked item using the fewest possible queries.

In this notebook:

* You choose a database size **N = 32**.
* Compute required number of qubits **n = log₂(N)**.
* Randomly select a marked index.
* Construct:

  * **Grover Oracle** (phase inversion of the marked state)
  * **Diffusion Operator** (inversion about mean)
* Compute the optimal number of iterations.
* Run the circuit on **Qiskit Aer Simulator**.
* Visualize the result using measurement histograms.

The outcome is a clear peak at the marked bitstring, demonstrating the algorithm’s correctness.

---

## Key Features

### ✔ Fully manual oracle construction

Implements a phase flip on the marked state using X gates + multi-controlled Z (via H-MCX-H).

### ✔ Full diffusion operator

Implements the inversion-about-mean operator exactly as defined in Grover’s algorithm.

### ✔ Optimal iteration count

Uses the theoretical expression:

[
t = \left\lceil \frac{\pi}{4\theta} - \frac12 \right\rceil , \quad
\theta = \arcsin\left(\frac{1}{\sqrt{N}}\right)
]

to maximize success probability.

### ✔ Clear visualization

Uses Qiskit’s `plot_histogram` to show how the marked state becomes the most probable outcome.

### ✔ Great for portfolio use

Well-structured and commented code suitable for learning and demonstration.

---

## How the Algorithm Works

1. **Superposition:**
   Hadamard gates prepare a uniform superposition over all N states.

2. **Oracle:**
   Flips the phase of the marked state (|w⟩).

3. **Diffusion Operator:**
   Reflects amplitudes about their average, amplifying the marked state.

4. **Iteration:**
   Oracle + Diffusion is repeated O(√N) times.

5. **Measurement:**
   The marked state appears with high probability.

---

## 📂 File Contents

* **Grover's_Algorithm.ipynb**
  Main notebook containing all code cells and Markdown explanations.

* **README.md**
  (this file) Documentation for understanding and running the project.

---

## Requirements

Install dependencies using:

```
pip install qiskit qiskit-aer matplotlib
```

---

## ▶ Running the Notebook

Open the notebook in Jupyter:

```
jupyter notebook Grover_Algorithm.ipynb
```

Then execute each cell sequentially.

The final histogram will highlight the marked element with high probability.

---

## Example Result

After completing the iterations, you should see a histogram where:

* The **marked bitstring** has the highest bar.
* Other states have minimal probability.

This confirms successful amplitude amplification.

---

## References

* Nielsen & Chuang — *Quantum Computation and Quantum Information*
* Qiskit Textbook: *Grover’s Algorithm*
* Grover, L. K. (1996). *A fast quantum mechanical algorithm for database search.*

---

## Conclusion

This notebook provides a clean and complete demonstration of Grover’s algorithm, implemented from scratch using Qiskit.
It is ideal for:

* Learning quantum algorithms
* Adding a strong project to your GitHub portfolio
* Showcasing practical understanding of quantum circuit construction

---

## Contributing

Feel free to fork this repository and submit pull requests if you want to experiment with higher qubit counts or run this on real backend hardware via IBM Quantum.
---
