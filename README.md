# Pauli Correlation Encoding for Optimization Problems

This repository implements **Pauli Correlation Encoding (PCE)** and related optimization techniques to solve combinatorial optimization problems such as the **Knapsack Problem**, **Max-Cut**, and **Maximum Independent Set**. It also includes tools for generating benchmark datasets, evaluating solutions, and checkpointing intermediate results.

---

## Features

### Key Implementations:
- **Pauli Correlation Optimizer**:
  - Enhanced with checkpointing for multi-round optimizations.
  - Reduces unused parameters for cleaner and efficient computations.

- **QUBO to MaxCut Transformation**:
  - Supports mapping Quadratic Unconstrained Binary Optimization (QUBO) problems to Weighted Max-Cut for improved quantum circuit-based approaches.

### Included Examples:
- Multi-dimensional Knapsack Problem (MDKP)
- Max-Cut Problem
- Maximum Independent Set (MIS)

---

## Repository Structure

- `mis_benchmark_instances/` - Benchmark datasets for solving the Maximum Independent Set problem.
- `multi_dim_kp_datasets/` - Datasets for multi-dimensional knapsack problems.
- `pce/` - Core implementation of Pauli Correlation Encoding and optimization routines.
- `qubo_to_maxcut/` - Tools to convert QUBO problems into Weighted Max-Cut formulations.
- **Notebooks**:
  - `knapsack.ipynb` - Demonstrates solving the knapsack problem using PCE.
  - `max_cut.ipynb` - Solves Max-Cut problems with the implemented methods.
  - `max_independent_set.ipynb` - Example for MIS problem solving.
  - `enumerate_all.ipynb` - Analyzes all solutions for certain small-scale problems.
  - `multi_dim_knapsack.ipynb` - Applies the PCE approach to multi-dimensional knapsack instances.
- **Checkpoints**:
  - `checkpoint_round_5.pkl`, `checkpoint_round_10.pkl`, `checkpoint_round_15.pkl` - Intermediate results for multi-round optimizations.
- `requirements.txt` - Python dependencies required to run the code.
- `qubo_results.csv` - Stores the results of QUBO problem transformations and optimizations.
- `README.md` - Project documentation (this file).

---

## Installation

1. Clone the repository:
```bash
   git clone https://github.com/MonitSharma/pauli_correlation_encoding.git
   cd pauli_correlation_encoding
```
2. Install dependencies:
```bash
   pip install -r requirements.txt
```
---

## Usage

### 1. Run the Notebooks

1. Launch Jupyter Notebook in the repository directory:
```bash
   jupyter notebook
```

2. Open the relevant `.ipynb` notebook based on the problem you want to solve:
   - `knapsack.ipynb` for the Knapsack Problem.
   - `max_cut.ipynb` for the Max-Cut Problem.
   - `max_independent_set.ipynb` for Maximum Independent Set (MIS).
   - `multi_dim_knapsack.ipynb` for multi-dimensional knapsack problems.
   - `enumerate_all.ipynb` for small-scale exhaustive solution enumeration.

3. Follow the steps in the notebook to execute the implemented algorithms, analyze datasets, or modify parameters.

---

### 2. Resume from Checkpoints

For iterative processes, the repository includes checkpoint files (e.g., `checkpoint_round_5.pkl`). You can load these files to resume optimization from a specific round. 

To load a checkpoint:
```bash
   import pickle

   with open('checkpoint_round_5.pkl', 'rb') as file:
       data = pickle.load(file)

   # Use the loaded data as input to continue your computations
```

---

### 3. QUBO to Max-Cut Transformation

Use the tools in the `qubo_to_maxcut/` directory to transform QUBO problems into Weighted Max-Cut problems. You can customize your input matrices and parameters for specific optimization tasks.

---

### 4. Results and Analysis

The results of QUBO transformations and optimizations are saved in `qubo_results.csv`. Use this file to:
- Analyze performance metrics.
- Compare multiple optimization approaches.
- Visualize outcomes using additional tools.

---

## Contributions

Contributions are welcome! Feel free to:
- Open issues for bugs or feature requests.
- Submit pull requests for enhancements or bug fixes.

---

## License

This project is licensed under the MIT License. See `LICENSE` for more details.

---

## Author

[Monit Sharma](https://github.com/MonitSharma)  
For queries, feel free to reach out or open an issue in the repository.

