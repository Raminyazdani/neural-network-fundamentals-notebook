# Neural Network Fundamentals

**Hands-on implementation of fundamental neural network concepts from scratch**

**Stack:** Python, Jupyter Notebook, NumPy, scikit-learn, PyTorch

## Overview

This project provides a practical exploration of neural network fundamentals through hands-on implementation. It covers core concepts including data generation for classification tasks, linear separability, decision boundaries, and the limitations of linear models on non-linear problems like XOR.

## Problem & Approach

**Problem:** Understanding neural networks requires practical experience with fundamental concepts including linear separability, decision boundaries, and the behavior of classification algorithms.

**Approach:**
- Generate synthetic datasets (linearly separable and XOR)
- Implement linear SVM classification using scikit-learn
- Visualize data clusters and decision boundaries
- Explore the limitations of linear models on non-linear problems
- Analyze the impact of outliers on decision boundaries

## Tech Stack

- Python 3.x
- NumPy - numerical computations and data generation
- Matplotlib - visualization of data and decision boundaries
- scikit-learn - SVM classification algorithms
- PyTorch - deep learning framework
- Jupyter Notebook - interactive development environment

## Repository Structure

```
.
├── neural_network_fundamentals.ipynb  # Main notebook with implementations
├── requirements.txt                    # Python dependencies
├── README.md                          # This file
└── .github/                           # GitHub configuration
```

## Setup / Installation

**Prerequisites:**
- Python 3.7 or higher
- pip package manager

**Install dependencies:**
```bash
pip install -r requirements.txt
```

**Alternative (using conda):**
```bash
conda create -n neural-net-fundamentals python=3.9
conda activate neural-net-fundamentals
pip install -r requirements.txt
```

## How to Run

1. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook neural_network_fundamentals.ipynb
   ```

2. **Run all cells** sequentially (Cell → Run All) or execute individually

3. **Expected runtime:** < 1 minute for all cells

## Data / Inputs

All data is **synthetic and generated within the notebook**:
- **Linearly separable dataset:** 200 points (2 clusters of 100 each) with Gaussian distribution
- **XOR dataset:** 4 points representing the classic XOR problem
- No external data files required
- Random seeds are set for reproducibility

## Outputs

The notebook produces:
- **Visualizations:** Scatter plots of data clusters with class labels
- **Decision boundaries:** Linear decision boundaries overlaid on data
- **Model predictions:** Classification results for test points
- **Analysis:** Observations on linear vs non-linear separability
- **Outlier analysis:** Impact of noisy data on decision boundaries

All outputs are displayed inline within the notebook.

## Key Concepts Demonstrated

1. **Data Generation:** Creating synthetic datasets for classification
2. **Linear Separability:** Understanding when linear models work
3. **SVM Classification:** Using LinearSVC for binary classification
4. **Decision Boundaries:** Visualizing how models separate classes
5. **Non-linear Problems:** Exploring XOR and limitations of linear models
6. **Robustness:** Analyzing the impact of outliers

## Reproducibility Notes

- Random seeds are set in the notebook (`np.random.seed()`)
- All dependencies specified in `requirements.txt`
- Tested on Python 3.9+
- No external configuration required
- All paths are relative to notebook location

## Troubleshooting

**Issue:** `ModuleNotFoundError` when running notebook
- **Solution:** Ensure all dependencies are installed: `pip install -r requirements.txt`

**Issue:** Jupyter not found
- **Solution:** Install Jupyter: `pip install jupyter`

**Issue:** Visualizations not displaying
- **Solution:** Ensure matplotlib backend is configured. Try adding `%matplotlib inline` at the top of the notebook.

**Issue:** Kernel crashes or hangs
- **Solution:** Restart the kernel (Kernel → Restart) and run cells again

## Notes

- Self-contained implementation (no external data required)
- Suitable for learning fundamental machine learning concepts
- Demonstrates practical applications of NumPy and scikit-learn
- Foundation for understanding more complex neural network architectures
