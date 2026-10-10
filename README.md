# COVID-19 CT Scan Classification

A deep learning project that classifies chest CT scan images into three categories using PyTorch and a pretrained MobileNetV3 model.

The project covers the main steps of an image classification workflow, from exploring the dataset and checking image quality to training the model and evaluating its performance on unseen test images.

## Dataset

The dataset was obtained from Kaggle:

[Preprocessed CT Scans for COVID-19](https://www.kaggle.com/datasets/azaemon/preprocessed-ct-scans-for-covid19)

It contains CT scan images organized into three classes:

- `NiCT`
- `nCT`
- `pCT`

The dataset contains **19,685 images** in total.

The original images are stored locally and are not included in this repository because of their size.

Please refer to the original Kaggle page for the dataset description, license, and usage conditions.

## Exploratory Data Analysis

Before training the model, I explored the dataset to understand its structure and identify potential issues.

The EDA included:

- Counting images in each class and examining class distribution.
- Checking images for loading errors or corrupted files.
- Examining image dimensions and comparing image sizes.
- Displaying sample images from each class.

The dataset contains an unequal number of images across the three classes, which is worth considering when interpreting the evaluation results.

## Model

The project uses **MobileNetV3 with transfer learning**.

The model was trained to classify CT scan images into the three dataset categories. Images were resized to `512 × 512` before being passed to the model.

Training and validation loss and accuracy were recorded to monitor the model's performance across epochs.

## Evaluation

The model was evaluated using a separate test set.

The evaluation included:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion matrix
- Training and validation curves

### Test Results

The model achieved the following overall results on the test set:

| Metric | Score |
|---|---:|
| Accuracy | 98.44% |
| Macro F1-score | 98.44% |
| Weighted F1-score | 98.44% |

### Per-Class Results

| Class | Precision | Recall | F1-score |
|---|---:|---:|---:|
| `NiCT` | 97.12% | 98.36% | 97.74% |
| `nCT` | 99.26% | 98.06% | 98.66% |
| `pCT` | 98.35% | 99.50% | 98.92% |

These results describe the model's performance on this dataset and should not be interpreted as evidence of clinical effectiveness.

## Technologies

- Python
- PyTorch
- Torchvision
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Pillow
- Scikit-learn
- Jupyter Notebook

## Project Structure

```text
COVID_CT_Classification/
├── dataset/
│   └── Original CT Scans/
│       ├── NiCT/
│       ├── nCT/
│       └── pCT/
├── models/
│   └── mobilenet_v3_ct.pth
├── notebooks/
│   ├── 01_data_exploration.ipynb
│   └── 02_model_training.ipynb
├── .gitignore
└── README.md
```

The dataset and trained model are stored locally and may not be available in the repository.

## Running the Project

1. Clone the repository.
2. Create and activate a Python virtual environment.
3. Install the required dependencies.
4. Download the dataset from Kaggle and place the images in the expected directory structure.
5. Open the notebooks in Jupyter Notebook or VS Code.
6. Run `01_data_exploration.ipynb` to explore the dataset.
7. Run `02_model_training.ipynb` to train and evaluate the model.

The notebooks contain the implementation and analysis for each stage of the project.

## Limitations

- The model was evaluated on a particular dataset and may not generalize to images from other sources.
- High test accuracy does not guarantee reliable performance in a clinical setting.
- Further testing on independent datasets would be needed to assess generalization.

## Disclaimer

This project was developed for educational and research purposes only. It is not a medical diagnostic tool and must not be used to diagnose COVID-19 or make medical decisions.