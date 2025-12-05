# BB84 Quantum Key Distribution (with Eve Intercept–Resend Attack)
This project implements the **BB84 quantum key distribution (QKD) protocol** using **Qiskit** on a classical simulator.  
It demonstrates how two parties (Alice and Bob) can securely share a key—and how the presence of an eavesdropper (Eve) increases the **Quantum Bit Error Rate (QBER)** to approximately **25%**.

---

## 🔍 Project Overview
This notebook simulates:

- Random bit generation  
- Random basis selection (Z-basis, X-basis)  
- Quantum state preparation by Alice  
- Eve performing **intercept–measure–resend**  
- Bob’s measurements  
- Basis comparison (sifting)  
- QBER calculation  
- Visualization of measurement outcomes  

It uses **Qiskit Aer’s QasmSimulator**, so no real quantum hardware is needed.

---

## 🧠 What BB84 Demonstrates

This project is a simulation of the **BB84 Protocol**, the first quantum cryptography protocol developed by Bennett and Brassard in 1984. 

The simulation uses **Qiskit** to demonstrate how two parties (Alice and Bob) can generate a shared secret key. Crucially, this project includes an **Eavesdropper (Eve)** performing an *Intercept-Resend attack* to demonstrate the fundamental security feature of QKD: **the presence of an eavesdropper introduces detectable statistical errors.**

## ⚙️ How It Works
The protocol relies on the **No-Cloning Theorem** and the principle that measuring a quantum state collapses it.

1. **Alice** prepares qubits in random states ($|0\rangle, |1\rangle, |+\rangle, |-\rangle$) using two bases ($Z$ and $X$).
2. **Eve (The Attacker)** intercepts the qubits, measures them in a random basis, and resends them to Bob.
3. **Bob** receives the qubits and measures them in random bases.
4. **Sifting:** Alice and Bob publicly compare their bases (not the bits). They keep only the bits where their bases matched.
5. **Error Check:** They compare a subset of the sifted key to calculate the **Quantum Bit Error Rate (QBER)**.

### The Physics of Detection
If Eve intercepts:
* She has a 50% chance of guessing the wrong basis.
* If she guesses wrong, she alters the state sent to Bob.
* Even if Bob measures in the correct basis, Eve's alteration gives him a 50% chance of getting the wrong result.
* **Theoretical QBER with Eve:** ~25%
* **Theoretical QBER without Eve:** 0% (in an ideal simulation)

---

## Key Features of This Implementation
- Full simulation of all BB84 steps  
- Eve’s measurement is explicitly modeled  
- Bitstrings reversed to match Alice's indices  
- QBER automatically computed  
- Histogram of measurement results  
- Clean Python structure suitable for teaching or portfolio use  

---

## Expected Output
- When Eve is present → **QBER ~ 0.25**  
- When Eve is removed → **QBER ~ 0**  
- Printed bitstrings for Alice, Eve, and Bob  
- Sifted keys (matching bases only)  
- Bar chart of outcome counts  

---

## 📁 File Structure
```
BB84/
│── BB84 Protocol-with Eve's interception.ipynb    # Main notebook
│── README.md              # This file
```

---

## How to Run
1. Install Qiskit:
   ```
   pip install qiskit qiskit-aer
   ```
2. Open the notebook:
   ```
   jupyter notebook BB84 Protocol-with Eve's interception.ipynb
   ```
3. Run all cells to generate the key and QBER.

---

## Requirements
- Python 3.0+  
- Qiskit  
- Qiskit Aer  
- Jupyter Notebook  

---

## Contributions
Pull requests and improvements are welcome!  
Feel free to fork the repo and submit enhancements.
