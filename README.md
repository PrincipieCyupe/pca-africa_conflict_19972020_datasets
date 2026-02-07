# PCA (Principal Components Analysis) on African Conflict Data 1997-2020

Principal Component Analysis implementation from scratch using NumPy, Pandas, and Matplotlib libraries on African conflict events dataset.

## Dataset
- **File:** `Africa_1997-2020_Jan08.csv`
- **Samples:** 65,535 conflict events across Africa
- **Features:** 10 numeric columns
- **Time Period:** January 1997 - January 2020

## Project Objective
Implement PCA from scratch to:
1. Reduce dimensionality (10D → 7D)
2. Retain maximum variance (0.88 or 88%)
3. Visualize transformation

## Installation

### Prerequisites
- Python 3.7 or higher
- Jupyter Notebook

### Required Libraries
Install dependencies using:
```bash
pip install -r requirements.txt
```

## Dependencies
- `numpy` - For numerical computations
- `pandas` - For data manipulation
- `matplotlib` - For visualizations

## How to Run

1. **Clone this repository:**
```bash
   git clone https://github.com/PrincipieCyupe/pca-africa_conflict_19972020_datasets.git
   cd pca-africa_conflict_19972020_datasets
```

2. **Install dependencies:**
```bash
   pip install -r requirements.txt
```

3. **Open Jupyter Notebook:**
```bash
   jupyter notebook
```

4. **Run the notebook:**
   - Open `PCA_Assignment.ipynb`
   - Run all cells sequentially (Cell → Run All)

## Results
- **Dimensionality Reduction:** 10 features → 7 principal components
- **Variance Retained:** 93.92%
- **Compression:** 20% reduction

### Principal Components:
| PC | Variance Explained | Cumulative Variance |
|----|-------------------|---------------------|
| PC1 | 22.47% | 22.47% |
| PC2 | 16.90% | 39.38% |
| PC3 | 11.25% | 50.63% |
| ... | ... | ... |
| PC7 | 5.53% | 88.38% |

## Project Structure
```
.
├── PCA_Assignment.ipynb          # Main notebook with PCA implementation
├── Africa_1997-2020_Jan08.csv    # Dataset
├── README.md                      # This file
└── requirements.txt               # Python dependencies
```

## Implementation Details

### Steps Implemented:
1. **Data Loading & Preprocessing**
   - Handle missing values if any
   - Select numeric columns only

2. **Standardization**
   - Manual implementation following the formula given: `(data - mean) / std`

3. **Covariance Matrix Calculation**
   - Using `np.cov()`

4. **Eigendecomposition**
   - Using `np.linalg.eig()`

5. **Sorting Principal Components**
   - Sort by eigenvalue (descending)

6. **Component Selection**
   - Dynamic selection based on 85% variance threshold
   - Selected 7 components (88.38% variance)

7. **Projection**
   - Transform data: `reduced_data = np.dot(standardized_data, eigenvectors)`

8. **Visualization**
   - Before/After PCA comparison

## Visualizations Included
- Original data scatter plot (first 2 features)
- Reduced data scatter plot (PC1 vs PC2)


## Author
Principie Cyubahiro - Machine Learning Engineer  

## Date
07/02/2026

## License
This project is for educational purposes (Advanced Linear Algebra course).
