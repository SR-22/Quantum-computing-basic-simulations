# Quantum-computing-basic-simulations
Includes basic quantum computing algorithms and protocols simulated using Qiskit and Aer simulator

# Quantum Algorithms & Protocols Simulations

This repository contains implementations of foundational quantum computing algorithms and protocols using **Qiskit** and the **Aer Simulator**.

The goal of this project is to demonstrate an understanding of quantum mechanics principles (superposition, entanglement, interference) and practical circuit design.

## 🛠️ Tools Used
* **Language:** Python 3.x
* **SDK:** Qiskit
* **Backend:** Qiskit Aer (Simulator)
* **Key Concepts:** Qubits, Quantum Gates, Measurement.

## 📂 Project Overview

### 1. Bell State Generation (Entanglement)
* **Description:** Created and measured the four Bell states to demonstrate quantum entanglement.
* **Key Learning:** Verified that measuring one qubit immediately determines the state of the other, illustrating non-local correlations.

### 2. BB84 Quantum Key Distribution
* **Description:** Simulated the BB84 protocol for secure key exchange between Alice and Bob.
* **Implementation:** Modeled the quantum channel, qubit preparation in X/Z bases, and basis reconciliation (sifting).
* **Noise Simulation:** Tested the protocol robustness by introducing simulated noise to mimic eavesdropping attempts.

### 3. Grover's Algorithm
* **Description:** Implemented Grover's search algorithm to find a marked element in an unstructured database.
* **Key Learning:** utilized Amplitude Amplification to increase the probability of measuring the correct state.

### 4. Quantum Random Number Generator (QRNG)
* **Description:** Built a true random number generator exploiting the inherent probabilistic nature of quantum measurement (collapsing superposition).

## 🚀 How to Run
1. Clone this repository.
2. Install dependencies:
   ```bash
   pip install qiskit qiskit-aer matplotlib jupyter
