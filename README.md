# Quantum Circuit for Portfolio Optimization

This repository demonstrates how to apply Quantum Computing techniques to solve the **Portfolio Optimization** problem. The goal is to select an optimal subset of assets to maximize returns while minimizing financial risk, utilizing a covariance matrix.

## 🚀 Features

The project explores three distinct approaches to solving the problem:

1. **Classical Optimization**: A brute-force classical method that iterates over all possible valid portfolios (i.e., selecting exactly 2 out of 4 assets) to calculate the objective score based on expected returns and risk.
2. **Quantum Kernel (Manual)**: Evaluates the overlap of quantum states (fidelity) mapped from asset features using `RY` gates. The resulting quantum kernel matrix is used to adjust the problem's cost matrix.
3. **Quantum Approximate Optimization Algorithm (QAOA)**: Manually constructs a QAOA circuit in Qiskit, applying problem (Cost) Hamiltonians via `RZZ` gates and Mixer Hamiltonians via `RX` gates to sample the most probable optimal portfolio.

## 📁 Repository Structure

* **`portfolio_qaoa.py`**: A complete Python script containing the implemented classical approach, quantum kernel state calculation, and the QAOA circuit compilation and execution.
* **`kernel.ipynb`**: A Jupyter Notebook providing a step-by-step walkthrough of the code, including visualizations of the quantum circuit and probability histograms of the measured results.

## 🛠️ Dependencies

Ensure you have the following Python packages installed to run the code:
* `numpy`
* `qiskit`
* `qiskit-aer`
* `matplotlib` (for notebook visualizations)

You can install them via pip:
```bash
pip install numpy qiskit qiskit-aer matplotlib
```

## 🏃 Usage

Run the Python script directly from your terminal:
```bash
python portfolio_qaoa.py
```

Or open the Jupyter Notebook to explore the steps interactively:
```bash
jupyter notebook kernel.ipynb
```
