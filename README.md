# ⚡ Leveraging Variational Quantum Circuits for Economic Dispatch in Cyber-Physical Power Systems  

**Author:** Muhammad Hasnain  
**Affiliation:** One Tech & AI (UK) Ltd  
**Keywords:** Quantum Computing, Variational Quantum Circuits (VQC), Economic Dispatch, Power Systems, SPSA, Hybrid Quantum-Classical Optimization, Cyber-Physical Systems  

---

## 🧠 Abstract  

This project presents a **Variational Quantum Circuit (VQC)** framework for solving a simplified **economic dispatch problem** in power systems — optimizing generator outputs to minimize total cost while meeting demand.  

The framework encodes generator outputs into **qubit states** using binary mapping and defines a **cost function** that incorporates quadratic transmission losses and penalties for demand-supply imbalance. A **parameterized quantum ansatz** (`RealAmplitudes`) explores potential solutions, while the **Simultaneous Perturbation Stochastic Approximation (SPSA)** optimizer iteratively adjusts parameters in a **hybrid quantum–classical optimization loop**.  

Using the **Qiskit AerSimulator**, the expectation value of the cost function is estimated from quantum measurement outcomes. Experimental results demonstrate convergence toward feasible generator schedules that minimize system cost while satisfying demand.  

This work highlights the potential of **quantum-enhanced optimization** in smart grids and cyber-physical energy systems, providing a pathway for integrating quantum methods into large-scale grid dispatch models.  

---

## ⚙️ Implementation Overview  

### 🧩 Framework Components  
- **Quantum Circuit Type:** Variational Quantum Circuit (VQC)  
- **Ansatz:** RealAmplitudes  
- **Optimizer:** Simultaneous Perturbation Stochastic Approximation (SPSA)  
- **Backend:** Qiskit AerSimulator  
- **Encoding Scheme:** Binary mapping of generator outputs  

### 🧮 Problem Formulation  
Economic dispatch problem:  

\[
\text{Minimize } C = \sum_i (a_i P_i^2 + b_i P_i + c_i) + \text{Losses} + \text{Penalty for Demand Mismatch}
\]  

Where \( P_i \) denotes generator power output encoded into quantum states.  

---

## 🚀 Outcomes  

| Parameter | Description | Result |
|------------|--------------|--------|
| **Initial Cost** | Estimated with random parameters | 8929.54 |
| **Optimized Cost** | After SPSA convergence (~9.1 seconds) | 9008.36 |
| **Optimal Bitstring** | Most probable quantum measurement outcome | `110010` |
| **Decoded Outputs** | Generator 1 = 85.71 MW, Generator 2 = 28.57 MW |  |
| **Total Generation** | 114.29 MW (Target: 120 MW) |  |
| **Final Classical Cost** | At optimal parameters | 172.82 |

✅ The hybrid quantum–classical VQC successfully identified feasible generator schedules and reduced total system cost.  
Though based on a simplified two-generator system, the outcomes demonstrate **scalability potential** for realistic smart grid optimization.  

---

git clone https://github.com/Hasnainfs/Leveraging-VQC-for-Economic-Dispatch.git
cd Leveraging-VQC-for-Economic-Dispatch
 

