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

## Setup / Installation

**Prerequisites:**
- Python 3.7 or higher
- pip package manager

**Install dependencies:**
```bash
pip install -r requirements.txt
```

## How to Run

1. **Launch Jupyter Notebook:**
   ```bash
   jupyter notebook neural_network_fundamentals.ipynb
   ```

2. **Run all cells** sequentially or execute individually

3. **Expected runtime:** < 1 minute for all cells

## Outputs

The notebook produces:
- **Visualizations:** Scatter plots of data clusters with class labels
- **Decision boundaries:** Linear decision boundaries overlaid on data
- **Model predictions:** Classification results for test points
- **Analysis:** Observations on linear vs non-linear separability

All outputs are displayed inline within the notebook.
