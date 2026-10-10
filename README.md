# COVID-19 CT Scan Classification

## Overview

This project explores CT scan images for COVID-19 classification using Python and data science tools.

The project starts with Exploratory Data Analysis (EDA) to understand the dataset, examine class distribution, and investigate image dimensions before developing machine learning models.

> **Disclaimer:** This is an educational and research project, not a medical diagnostic tool.

## Dataset

The dataset is organized into three classes:

- `nCT`
- `NiCT`
- `pCT`

The original dataset is stored locally and is not included in this repository.

### Dataset Source

The dataset used in this project is obtained from Kaggle:

**[Preprocessed CT Scans for COVID-19](https://www.kaggle.com/datasets/azaemon/preprocessed-ct-scans-for-covid19)**

The dataset contains preprocessed CT scan images organized into three classes:

- `nCT`
- `NiCT`
- `pCT`

The dataset is stored locally and is not included in this repository because of its size.

**License:** Please refer to the original Kaggle dataset page for the applicable license and usage conditions.

**Note:** The dataset is used for educational and research purposes only. This project is not intended for clinical diagnosis.

## Technologies

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Pillow
- Jupyter Notebook
- Scikit-learn

## Project Structure

```text
COVID-CT-Classification/
├── .gitignore
├── README.md
└── notebooks/
    ├── 01_data_exploration.ipynb
    └── 02_model_training.ipynb