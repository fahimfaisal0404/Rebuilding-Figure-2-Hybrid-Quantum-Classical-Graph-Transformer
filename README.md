# Rebuilding Figure 2 — Hybrid Quantum-Classical Graph Transformer

This project recreates **Figure 2** from the paper *“Hybrid Quantum-Classical Graph Transformers for Efficient Sentiment Analysis”* using **Qiskit** and **Qiskit Aer**.

### What I implemented

* **Amplitude encoding:** 768-dimensional vector → padded to 1024 → 10-qubit state.
* **Query circuit \(U_Q(\theta)\):** Rx → Ry → Rz → CNOT ring → Ry → QFT.
* **Pauli measurements:** X, Y, and Z on each of the 10 qubits → 30-dimensional query vector.
* **Exact simulation:** Compared Aer results with Qiskit's `Statevector`.
* **Shot-based simulation:** Tested 100, 1,000, 10,000, and 100,000 shots and calculated RMSE.
* **Attention score:** Calculated the scaled dot product between the query and key vectors.

### Important Note

This is an **educational reconstruction**, not a full reproduction of the paper. I used a random input vector and random circuit parameters; there is no training, sentiment dataset, or accuracy evaluation.

### Requirements

```bash
pip install qiskit qiskit-aer matplotlib pylatexenc
```

### Reference

Aktar, Bartschi, Badawy, and Eidenbenz,
*Hybrid Quantum-Classical Graph Transformers for Efficient Sentiment Analysis.*


<img width="2640" height="889" alt="image" src="https://github.com/user-attachments/assets/cac3ea5a-145d-4a55-b841-5e179c89709c" />

<img width="900" height="630" alt="image" src="https://github.com/user-attachments/assets/fb97383e-2d9a-4d70-b8fd-7a246939f218" />

