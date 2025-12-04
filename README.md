# SDSS DR18 Galaxy Classification (Machine Learning Project)

This repository contains a machine learning pipeline for classifying galaxies using photometric data from the Sloan Digital Sky Survey (SDSS) Eighteenth Data Release (DR18). The goal of the project is to predict whether a galaxy belongs to the **STARFORMING** or **STARBURST** subclass based on its photometric and structural features.

The dataset includes **100,000 galaxy observations**, each with a variety of features such as sky position (RA/DEC), photometric magnitudes, axis ratios, redshift, and other SDSS-derived parameters. This project demonstrates the end-to-end machine learning workflow including data preprocessing, exploratory analysis, model training, evaluation, and comparison.

## Project Overview

This project includes:

- Loading and inspecting SDSS DR18 galaxy data
- Data preprocessing and cleaning
- Exploratory Data Analysis (EDA) with visualizations
- Feature scaling and selection
- Training two supervised machine learning models:
  - Logistic Regression (multinomial)
  - Random Forest Classifier
- Model evaluation using accuracy, confusion matrix, and classification report
- Comparative analysis of model performance
- A fully documented Jupyter Notebook

The goal is to determine how well SDSS photometric and structural features can classify galaxies into the STARFORMING and STARBURST subclasses.

## Dataset Description

This dataset originates from the Sloan Digital Sky Survey (SDSS), one of the largest astronomical surveys ever conducted. SDSS has observed roughly one-third of the sky and cataloged nearly 3 million galaxies.

The dataset used here contains:

- **100,000 galaxy entries**
- **Photometric features:** including magnitudes and band-specific axis ratios (e.g., expAB_u, expAB_g, … expAB_z)
- **Coordinates:** right ascension (ra) and declination (dec)
- **Redshift and redshift error**
- **Subclass labels:** only two galaxy types are included:
  - STARFORMING
  - STARBURST

Dataset source information:
The Sloan Digital Sky Surveys. SDSS DR18 SkyServer SQL Access: https://skyserver.sdss.org/dr18/SearchTools/sql#.

Scientific reference:
Almeida, A., et al. (2023). The Eighteenth Data Release of the Sloan Digital Sky Surveys: Targeting and First Spectra from SDSS-V. NASA ADS. https://doi.org/10.48550/arXiv.2301.07688

This dataset provides a rich feature set suitable for binary classification.

## Repository Structure
```
.
├── data/                     
├── notebook/
│   └── galaxy_classification.ipynb
├── figs/                     
├── src/                      
└── README.md
```
Descriptions:
- data/ — optional folder for storing the dataset
- notebook/ — main Jupyter notebook for analysis
- figs/ — saved plots (EDA figures, confusion matrices, etc.)
- src/ — optional helper scripts
- README.md — project documentation

## Machine Learning Models

### Logistic Regression
- Serves as an interpretable baseline model
- Uses a linear decision boundary for binary classification
- Allows examination of which features influence the prediction most strongly

### Random Forest Classifier
- Nonlinear ensemble learning method
- Captures feature interactions and complex patterns
- Provides feature importance scores
- Expected to outperform linear models on astrophysical data

Both models are trained, evaluated, and compared to determine which performs better on SDSS DR18 galaxy subclassification.

## Author

Gavin Sacek-Brooks
Computer Science Student
