# A Machine Learning Framework for Predicting Cancer Risk in Type 2 Diabetes Using Simulated Continuous Glucose Monitoring Data

## Overview

This repository contains the code, synthetic data, and documentation for research on predicting cancer risk among individuals with Type 2 diabetes using machine learning algorithms and simulated continuous glucose monitoring (CGM) data. The project aims to develop and evaluate a Random Forest-based framework for early detection of cancer risk, leveraging key glycemic and clinical features extracted from a synthetic cohort.

## Contents

- `AI_Prediction_Diabetes.ipynb` – Main Jupyter notebook for data processing, model training, evaluation, and visualization.
- `data/` – Folder for synthetic CGM datasets.
- `src/` – Source code for data generation, feature engineering, and model utilities.
- `results/` – Output metrics, figures, and model artifacts.
- `README.md` – Project documentation (this file).

## Project Description

Accurate risk prediction for cancer among patients with Type 2 diabetes is essential for improving clinical outcomes. This study simulates CGM profiles for 500 patients, generates relevant clinical and glycemic features, and applies a Random Forest classifier to detect elevated cancer risk. Model performance is evaluated using accuracy, ROC AUC, precision, recall, and F1-score, with cross-validation to ensure robustness. The approach demonstrates the potential of synthetic data and machine learning for clinical risk stratification.

## Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook
- Required Python packages (see `requirements.txt`):
  - pandas
  - numpy
  - scikit-learn
  - matplotlib
  - seaborn

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/bakhita11/A-Machine-Learning-Framework-for-Predicting-Cancer-Risk-in-Type-2-Diabetes.git
   cd A-Machine-Learning-Framework-for-Predicting-Cancer-Risk-in-Type-2-Diabetes
   ```
2. (Optional) Create and activate a virtual environment.
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Usage

1. Use the data generation code 
2. Open and run `AI_Prediction_Diabetes.ipynb` in Jupyter Notebook or JupyterLab.
3. Review results, figures, and metrics in the `results/` folder.

## Results

- Achieved detection accuracy: **93.2%**
- ROC AUC: **0.945**
- Precision, Recall, F1-score: **0.93**
- Five-fold cross-validation mean AUC: **0.944 (SD 0.004)**
- Top predictive features identified through feature selection.

## Citation

If you use this code or data in your research, please cite:

> Bakhita Salman, et al. "A Machine Learning Framework for Predicting Cancer Risk in Type 2 Diabetes Using Simulated Continuous Glucose Monitoring Data." (2025).

## License

This project is licensed under the MIT License.

## Contact

For questions or collaboration, contact:  
Bakhita Salman  
TAMIU
bakhita.salman@tamiu.edu

 
