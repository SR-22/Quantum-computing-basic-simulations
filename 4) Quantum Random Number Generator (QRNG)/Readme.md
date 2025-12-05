# Quantum Random Number Generator (QRNG) with Qiskit

This repository contains two different implementations of a Quantum Random Number Generator (QRNG) using IBM's Qiskit framework. Unlike Classical Pseudo-Random Number Generators (PRNGs), which rely on deterministic mathematical formulas, these generators rely on the fundamental unpredictability of quantum mechanics.



## The Concept

In classical computing, bits are deterministic (0 or 1). In quantum computing, we can place a qubit in a state of **superposition** using a Hadamard Gate ($H$).

$$H|0\rangle = \frac{|0\rangle + |1\rangle}{\sqrt{2}}$$

When we measure this qubit, the superposition collapses to either a 0 or a 1 with exactly 50% probability. This physical process is inherently random, making it an ideal source for random number generation.

## 📂 Repository Contents

This project includes two Jupyter Notebooks, each demonstrating a different strategy for generating random bits.

### 1. The Parallel Approach (`QRNG_function.ipynb`)
**Strategy:** *Spatial Parallelism*
* **Method:** To generate an $N$-bit number, this script creates a quantum circuit with $N$ distinct qubits.
* **Execution:** It applies the Hadamard gate to all qubits simultaneously and measures them in a single "shot" (execution).
* **Use Case:** This is functionally efficient when you want to generate a specific bit-depth number (e.g., an 8-bit integer) instantly using a Python function.

### 2. The Serial/Simulator Approach (`QRNG_simulator.ipynb`)
**Strategy:** *Temporal Repetition*
* **Method:** This script uses a single qubit and runs the experiment repeatedly ($N$ shots) to generate a sequence of bits.
* **Visualization:** Includes circuit diagrams and measurement histograms to visually verify the uniform distribution of randomness.
* **Outputs:** Demonstrates how to convert the binary stream into:
    * Integer lists
    * Large Integers
    * Hexadecimal strings (commonly used in cryptography)

## Comparison of Approaches

| Feature | Parallel Approach | Serial Approach |
| :--- | :--- | :--- |
| **Qubits Used** | $N$ Qubits | 1 Qubit |
| **Circuit Shots** | 1 Shot | $N$ Shots |
| **Hardware** | Requires larger quantum volume | Minimal hardware requirement |
| **Best For** | Clean function integration | Education, visualization, & streaming |

### Prerequisites
To run these notebooks, you will need Python installed along with the Qiskit SDK.

``pip install qiskit qiskit-aer matplotlib``

## Usage
Clone this repository.

Open the notebooks using Jupyter Lab or VS Code.

Run the cells to generate your own quantum random numbers!

## License

This project is open source. Feel free to use the code for educational purposes or as a starting point for more complex quantum algorithms.
