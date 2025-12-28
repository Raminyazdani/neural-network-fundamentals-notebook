# Git Development History: Neural Network Fundamentals

## History Expansion Note (v3)

This historian run expands the previous 14-step history into a more granular 21-step development timeline, meeting the requirement of at least 1.5× expansion.

**Expansion Metrics:**
- **N_old:** 14 steps (previous v2 run)
- **N_target:** ceil(14 × 1.5) = 21 steps (minimum required)
- **N_achieved:** 21 steps ✓
- **Achieved multiplier:** 21 / 14 = **1.50×** (exactly meets requirement)

**Mapping from Old Steps (v2) to New Steps (v3):**

| Old Step | Old Summary | New Steps | New Summary |
|----------|-------------|-----------|-------------|
| 01 | Initial repository setup | 01 | Initial repository setup (unchanged) |
| 02 | Linearly separable data | 02-03 | Split: scaffold (02) + implementation (03) |
| 03 | XOR dataset | 04 | XOR dataset generation (unchanged) |
| 04 | Data visualization (OOPS) | 05 | Data visualization with wrong import (OOPS) |
| 05 | Fix matplotlib import (HOTFIX) | 06 | Fix matplotlib import (HOTFIX) |
| 06 | Linear SVM | 07-08 | Split: import sklearn (07) + implementation (08) |
| 07 | Visualization function | 09 | Decision boundary function (unchanged) |
| 08 | Application | 10-11 | Split: basic viz (10) + enhanced XOR (11) |
| — | **NEW** | 12-13 | **NEW OOPS→HOTFIX:** typo in requirements.txt (12) + fix (13) |
| 09 | RBF kernel | 14-15 | Split: kernel addition (14) + parameter tuning (15) |
| 10 | Analysis documentation | 16 | Analysis documentation (unchanged) |
| 11 | Outlier generation | 17-18 | Split: outlier logic (17) + integration (18) |
| 12 | Impact analysis | 19 | Outlier impact analysis (unchanged) |
| 13 | Documentation | 20 | Documentation enhancement (unchanged) |
| 14 | Portfolio refinement | 21 | Final portfolio refinement (unchanged) |

**OOPS→HOTFIX Sequences:**

This expansion includes **TWO** oops→hotfix pairs to demonstrate realistic development workflow:

1. **Steps 05-06 (Matplotlib Import Error):**
   - **What broke (Step 05):** Used wrong matplotlib import (`from matplotlib import plot` instead of `import matplotlib.pyplot as plt`)
   - **How noticed:** This would cause AttributeError when trying to use pyplot functions
   - **How fixed (Step 06):** Corrected to standard matplotlib convention using `import matplotlib.pyplot as plt`
   - **Why realistic:** Import path mistakes are common when quickly implementing visualization code

2. **Steps 12-13 (Dependency Typo - NEW):**
   - **What broke (Step 12):** Typo in requirements.txt (`toch>=2.0.0` instead of `torch>=2.0.0`)
   - **How noticed:** Would cause pip install failure with "No matching distribution found for toch"
   - **How fixed (Step 13):** Removed the unnecessary torch dependency entirely (not used in this notebook)
   - **Why realistic:** Typos in dependency files are common, especially when adding/removing packages quickly

---

## Development Timeline

### Step 01: Initial Repository Setup
**Commit:** "Initial commit: project structure and dependencies"  
**Date:** 2024-10-15

**Summary:**
- Created repository with basic structure
- Added README.md with project overview
- Created requirements.txt with initial dependencies (numpy, matplotlib, jupyter)
- Added .gitignore for Python projects
- Established project foundation

**Files Created:**
- README.md (initial version with overview)
- requirements.txt (numpy>=1.21.0, matplotlib>=3.3.0, jupyter>=1.0.0)
- .gitignore (Python standard ignores)

**Changes:**
- Initial project scaffolding
- Dependencies specification
- Basic documentation structure

---

### Step 02: Linearly Separable Data - Scaffold
**Commit:** "Add scaffold for linearly separable data generation"  
**Date:** 2024-10-16 (morning)

**Summary:**
- Created initial notebook structure
- Added title and section headers
- Set up markdown documentation for data generation
- Prepared structure for implementation

**Added:**
- neural_network_fundamentals.ipynb (initial cells)
  - Title cell: "# Neural Network Fundamentals"
  - Section header: "## Linearly Separable Data Generation"
  - Description of what will be implemented

**Changes:**
- Created notebook file with foundational structure
- 2 markdown cells (title + section)

---

### Step 03: Linearly Separable Data - Implementation
**Commit:** "Implement linearly separable data generation function"  
**Date:** 2024-10-16 (afternoon)

**Summary:**
- Implemented function to generate linearly separable 2D clusters
- Uses NumPy for data creation with Gaussian distribution
- Generates two clusters that can be separated by a linear boundary
- Added imports and complete implementation

**Updated:**
- neural_network_fundamentals.ipynb
  - Added imports (numpy, matplotlib.pyplot)
  - Implemented `generate_linearly_separable_data()` function
  - Function creates 100 points per cluster with controllable separation
  - Returns X (features) and y (labels)

**Changes:**
- Added code cell with data generation implementation
- 3 cells total (2 markdown, 1 code)

---

### Step 04: XOR Dataset Generation
**Commit:** "Add XOR dataset generation"  
**Date:** 2024-10-16 (evening)

**Summary:**
- Implemented XOR dataset generation
- Classic non-linearly separable problem
- Uses 4 points representing XOR logic gate
- Demonstrates limitation of linear models

**Updated:**
- neural_network_fundamentals.ipynb
  - Added "## XOR Dataset Generation" section (markdown)
  - Implemented `generate_xor_data()` function (code)
  - Creates the 4 XOR points: (0,0)→0, (0,1)→1, (1,0)→1, (1,1)→0

**Changes:**
- Added 2 cells (1 markdown, 1 code)
- 5 cells total

---

### Step 05: Data Visualization - OOPS (Wrong Import)
**Commit:** "Add data visualization function (WIP)"  
**Date:** 2024-10-17 (morning)

**Summary:**
- Added visualization function to display 2D data points
- **BUG INTRODUCED:** Used incorrect matplotlib import
- Function implementation is correct but import statement is wrong
- Would cause runtime error when executed

**Updated:**
- neural_network_fundamentals.ipynb
  - Added "## Data Visualization" section (markdown)
  - Added `visualize_data()` function with scatter plots
  - **MISTAKE:** Used `from matplotlib import plot` (wrong module)
  - Function includes: figure creation, scatter plots, labels, legend, grid

**Changes:**
- Added 2 cells (1 markdown, 1 code)
- 7 cells total
- **Note:** This step contains a deliberate bug (wrong import)

---

### Step 06: Fix Matplotlib Import - HOTFIX
**Commit:** "Fix matplotlib import statement"  
**Date:** 2024-10-17 (late morning)

**Summary:**
- Fixed matplotlib import error discovered during testing
- Changed to proper matplotlib.pyplot convention
- All plotting functions now work correctly
- Quick hotfix after noticing the import issue

**Updated:**
- neural_network_fundamentals.ipynb
  - **FIXED:** Changed `from matplotlib import plot` to `import matplotlib.pyplot as plt`
  - Visualization function now uses correct matplotlib API
  - All other code remains the same

**Changes:**
- Fixed 1 line in code cell
- 7 cells total (bug resolved)

---

### Step 07: Linear SVM - Import sklearn
**Commit:** "Add scikit-learn import for SVM"  
**Date:** 2024-10-17 (afternoon)

**Summary:**
- Added scikit-learn to dependencies
- Imported LinearSVC for classification
- Set up section for SVM implementation
- Prepared for model training

**Updated:**
- requirements.txt
  - Added scikit-learn>=1.0.0
- neural_network_fundamentals.ipynb
  - Added "## Linear SVM Classification" section (markdown)
  - Added import statement: `from sklearn.svm import LinearSVC`

**Changes:**
- Updated requirements.txt (added sklearn)
- Added 2 cells to notebook (1 markdown, 1 code with import)
- 9 cells total

---

### Step 08: Linear SVM - Implementation
**Commit:** "Implement Linear SVM classification"  
**Date:** 2024-10-17 (late afternoon)

**Summary:**
- Generated linearly separable data and visualized it
- Trained Linear SVM classifier on the data
- Calculated and displayed accuracy
- Completed basic classification pipeline

**Updated:**
- neural_network_fundamentals.ipynb
  - Generated data using `generate_linearly_separable_data()`
  - Visualized data with `visualize_data()`
  - Trained LinearSVC model
  - Printed accuracy score

**Changes:**
- Updated code cell with full SVM training pipeline
- 9 cells total (implementation complete)

---

### Step 09: Decision Boundary Visualization Function
**Commit:** "Add decision boundary visualization function"  
**Date:** 2024-10-18 (morning)

**Summary:**
- Implemented comprehensive decision boundary plotting
- Uses meshgrid to create dense grid of points
- Predicts class for each point to show boundary
- Visualizes with contour plot and scatter

**Updated:**
- neural_network_fundamentals.ipynb
  - Added "## Decision Boundary Visualization" section (markdown)
  - Implemented `plot_decision_boundary()` function
  - Function creates 2D mesh, predicts on grid, plots contour

**Changes:**
- Added 2 cells (1 markdown, 1 code)
- 11 cells total

---

### Step 10: Apply Decision Boundary Visualization - Basic
**Commit:** "Visualize decision boundary for linear data"  
**Date:** 2024-10-18 (late morning)

**Summary:**
- Applied decision boundary visualization to linearly separable data
- Shows how Linear SVM creates clean separation
- Demonstrates successful classification on linear problem

**Updated:**
- neural_network_fundamentals.ipynb
  - Added code to visualize decision boundary for linear SVM
  - Call: `plot_decision_boundary(X_linear, y_linear, svm_linear, ...)`

**Changes:**
- Added 1 code cell
- 12 cells total

---

### Step 11: Apply to XOR - Enhanced
**Commit:** "Apply Linear SVM to XOR dataset"  
**Date:** 2024-10-18 (afternoon)

**Summary:**
- Generated XOR dataset and visualized it
- Attempted Linear SVM on XOR (non-linear problem)
- Demonstrated limitation: poor accuracy on XOR
- Visualized decision boundary showing linear limitation

**Updated:**
- neural_network_fundamentals.ipynb
  - Generated XOR data
  - Trained Linear SVM on XOR
  - Printed accuracy (low, as expected)
  - Visualized poor decision boundary

**Changes:**
- Added 1 code cell with XOR experiment
- 13 cells total

---

### Step 12: Wrong Dependency - OOPS (Typo in requirements.txt)
**Commit:** "Update dependencies for advanced models"  
**Date:** 2024-10-18 (late afternoon)

**Summary:**
- Attempted to add PyTorch dependency for future work
- **BUG INTRODUCED:** Typo in package name (`toch` instead of `torch`)
- Would cause pip install to fail
- Realistic mistake when quickly editing dependency file

**Updated:**
- requirements.txt
  - Added line: `toch>=2.0.0` (typo - should be `torch`)
  - **MISTAKE:** Package name misspelled

**Changes:**
- Updated requirements.txt (with typo)
- **Note:** This step contains a deliberate bug

---

### Step 13: Fix Dependency - HOTFIX
**Commit:** "Fix requirements.txt - remove unused torch dependency"  
**Date:** 2024-10-18 (evening)

**Summary:**
- Noticed typo in requirements.txt during pip install
- Realized torch is not actually needed for this notebook
- Removed the incorrect dependency line entirely
- Quick fix to unblock development

**Updated:**
- requirements.txt
  - **FIXED:** Removed the typo line (`toch>=2.0.0`)
  - Final dependencies: numpy, matplotlib, scikit-learn, jupyter
  - All dependencies are actually used in the notebook

**Changes:**
- Fixed requirements.txt (removed typo)
- Clean dependency list

---

### Step 14: RBF Kernel Addition
**Commit:** "Add RBF kernel SVM for XOR"  
**Date:** 2024-10-19 (morning)

**Summary:**
- Added non-linear SVM using RBF kernel
- Imported SVC (full SVM with kernel support)
- Trained on XOR dataset to show improvement
- Initial implementation without parameter tuning

**Updated:**
- neural_network_fundamentals.ipynb
  - Added "## Model Optimization" section (markdown)
  - Imported `from sklearn.svm import SVC`
  - Trained RBF SVM on XOR: `SVC(kernel='rbf')`
  - Printed accuracy (much better than linear)

**Changes:**
- Added 2 cells (1 markdown, 1 code)
- 15 cells total

---

### Step 15: RBF Parameter Tuning
**Commit:** "Tune RBF kernel parameters and visualize"  
**Date:** 2024-10-19 (late morning)

**Summary:**
- Added explicit parameters to RBF kernel (gamma, C)
- Optimized for XOR problem
- Visualized decision boundary showing perfect separation
- Demonstrated power of non-linear kernels

**Updated:**
- neural_network_fundamentals.ipynb
  - Updated RBF SVM with parameters: `gamma='scale', C=1.0`
  - Added decision boundary visualization for RBF on XOR
  - Shows complex non-linear boundary that perfectly separates XOR

**Changes:**
- Updated code cell with parameters and visualization
- 15 cells total

---

### Step 16: Analysis Documentation
**Commit:** "Add observations on linear vs non-linear classification"  
**Date:** 2024-10-19 (afternoon)

**Summary:**
- Documented key observations from experiments
- Explained when linear models work vs fail
- Described power of non-linear kernels
- Provided insights for understanding

**Updated:**
- neural_network_fundamentals.ipynb
  - Added "## Observations: Linear vs Non-Linear Classification" section
  - Documented: Linear models work for linearly separable data
  - Documented: Non-linear kernels (RBF) handle complex boundaries
  - Explained XOR as classic non-linear problem

**Changes:**
- Added 1 markdown cell
- 16 cells total

---

### Step 17: Outlier Generation Logic
**Commit:** "Implement outlier generation function"  
**Date:** 2024-10-20 (morning)

**Summary:**
- Created function to add outliers to dataset
- Outliers generated by flipping labels randomly
- Simulates noisy/mislabeled data
- Prepared for robustness analysis

**Updated:**
- neural_network_fundamentals.ipynb
  - Added "## Impact of Outliers on Decision Boundary" section
  - Implemented `add_outliers()` function
  - Function randomly flips n labels to create noise

**Changes:**
- Added 2 cells (1 markdown, 1 code)
- 18 cells total

---

### Step 18: Outlier Integration
**Commit:** "Generate and visualize data with outliers"  
**Date:** 2024-10-20 (late morning)

**Summary:**
- Applied outlier generation to linearly separable data
- Created dataset with 10 flipped labels
- Visualized noisy dataset
- Set up for impact analysis

**Updated:**
- neural_network_fundamentals.ipynb
  - Generated data with outliers using `add_outliers()`
  - Visualized noisy dataset
  - Shows some misclassified points (flipped labels)

**Changes:**
- Added 1 code cell
- 19 cells total

---

### Step 19: Outlier Impact Analysis
**Commit:** "Analyze impact of outliers on decision boundary"  
**Date:** 2024-10-20 (afternoon)

**Summary:**
- Trained Linear SVM on noisy data
- Calculated accuracy (lower than clean data)
- Visualized decision boundary with outliers
- Demonstrated impact of noise on classification

**Updated:**
- neural_network_fundamentals.ipynb
  - Trained Linear SVM on outlier data
  - Printed accuracy (degraded due to noise)
  - Visualized decision boundary showing impact
  - Boundary affected by mislabeled points

**Changes:**
- Added 1 code cell
- 20 cells total (all content implemented)

---

### Step 20: Documentation Enhancement
**Commit:** "Enhance README with comprehensive documentation"  
**Date:** 2024-10-21

**Summary:**
- Upgraded README to portfolio-grade standards
- Added detailed sections for setup, usage, troubleshooting
- Documented stack, structure, inputs/outputs
- Professional presentation of project

**Updated:**
- README.md
  - Added comprehensive overview and problem statement
  - Added detailed tech stack with descriptions
  - Added repository structure diagram
  - Added step-by-step setup instructions (pip + conda)
  - Added clear run instructions
  - Added data/inputs section (synthetic data)
  - Added outputs section
  - Added key concepts demonstrated
  - Added reproducibility notes
  - Added troubleshooting section

**Changes:**
- Complete README overhaul (portfolio-ready)

---

### Step 21: Final Portfolio Refinement
**Commit:** "Final portfolio refinement - remove academic traces"  
**Date:** 2024-10-23

**Summary:**
- Final cleanup to make project portfolio-ready
- Removed all assignment/academic language from notebook
- Ensured professional presentation throughout
- Finalized all documentation
- This step matches the current repository state exactly

**Updated:**
- neural_network_fundamentals.ipynb
  - Professional markdown sections throughout
  - No assignment references
  - Clean, educational presentation
  - 19 cells total (10 markdown, 9 code)
- README.md
  - Portfolio-grade documentation
  - Comprehensive and professional
- requirements.txt
  - Only necessary dependencies: numpy, matplotlib, scikit-learn, jupyter
  - No unused packages

**Changes:**
- Final polish on all files
- Repository is portfolio-ready
- All academic traces removed
- Professional naming and structure throughout

---

## Repository State Verification

**Final Snapshot (Step 21) Contents:**
```
step_21/
├── .gitignore
├── README.md
├── neural_network_fundamentals.ipynb
└── requirements.txt
```

**Snapshot Integrity:**
- ✅ All 21 steps created with sequential integer naming (step_01 to step_21)
- ✅ No snapshot contains `history/` directory (no recursion)
- ✅ No snapshot contains `.git/` directory
- ✅ Step 21 matches current repository state exactly (excluding .github, history, ledger files)
- ✅ Progressive implementation from minimal setup to complete portfolio-ready state
- ✅ Two realistic OOPS→HOTFIX sequences included (steps 05-06, steps 12-13)

**Timeline Summary:**
- Development period: October 15-23, 2024 (9 days)
- Total commits: 21 incremental commits
- Workflow demonstrates: initial setup → feature implementation → bugs → immediate fixes → optimization → documentation → portfolio refinement

**Expansion Achievement:**
- N_old: 14 steps
- N_target: 21 steps (ceil(14 × 1.5) = 21)
- N_achieved: 21 steps ✓
- Multiplier: 1.50× (exactly meets 1.5× requirement)
