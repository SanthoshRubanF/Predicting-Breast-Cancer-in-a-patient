# Predicting Breast Cancer using Machine Learning

## Overview

This project aims to predict whether a patient has breast cancer ('Benign' or 'Malignant') based on details of cell nuclei taken from a breast mass. The project utilizes various machine learning algorithms, including Support Vector Machines (SVM) and ensemble techniques (Random Forest, AdaBoost), to accurately classify the data.

## Dataset

The dataset (`cancer.csv`) contains several predictor variables and one target variable, `Diagnosis`.

*   **Target Variable**:
    *   `Diagnosis`: 'Benign' (0) meaning cells are not harmful, or 'Malignant' (1) meaning the patient has cancer.

*   **Predictor Variables (30 features)**:
    These features represent the mean, standard error (SE), and "worst" or largest values of various cell nuclei characteristics computed for each image:
    *   `radius`: Mean of distances from center to points on the perimeter
    *   `texture`: Standard deviation of gray-scale values
    *   `perimeter`: Observed perimeter of the lump
    *   `area`: Observed area of lump
    *   `smoothness`: Local variation in radius lengths
    *   `compactness`: perimeter^2 / area - 1.0
    *   `concavity`: Severity of concave portions of the contour
    *   `concave points`: Number of concave portions of the contour
    *   `symmetry`: Lump symmetry
    *   `fractal dimension`: "coastline approximation" - 1

## Methodology

1.  **Exploratory Data Analysis (EDA)**:
    *   Analyzing the dataset structure and handling missing values.
    *   Visualizing feature distributions using count plots and boxplots.
    *   Exploring correlations between features using heatmaps.

2.  **Data Pre-processing**:
    *   Encoding the categorical target variable.
    *   Splitting the data into training and testing sets (80/20 split).
    *   Scaling features using `StandardScaler` to ensure features are on a similar scale (vital for distance-based algorithms like SVM).

3.  **Model Training & Evaluation**:
    *   **Baseline Models**: Logistic Regression and a baseline Support Vector Machine (SVM).
    *   **Ensemble Techniques**: Random Forest Classifier and AdaBoost Classifier, demonstrating powerful handling of complex datasets.
    *   **Hyperparameter Tuning**: Using `GridSearchCV` to find the optimal parameters (`C`, `kernel`, `gamma`) for the SVM model.

4.  **Performance Metrics**:
    Models are evaluated comprehensively using metrics beyond simple accuracy:
    *   **Accuracy**
    *   **Precision**
    *   **Sensitivity (Recall)**
    *   **Specificity**
    *   **AUC ROC** (Area Under the Receiver Operating Characteristic Curve)

## Results

A comparison table is generated at the end of the notebook, providing a side-by-side view of each model's performance based on the metrics listed above. Based on evaluations, the fine-tuned SVM model and the ensemble techniques offer high accuracy and robust predicting capabilities.

## How to Run

1.  **Environment Setup**:
    Ensure you have Python installed along with the necessary libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, and `scikit-learn`.

    You can use the local virtual environment provided in the `.venv` folder.

2.  **Execution**:
    *   Open `Predicting Breast Cancer.ipynb` using Jupyter Notebook, JupyterLab, or Google Colab.
    *   Run the cells sequentially from top to bottom.
    *   Ensure `cancer.csv` is located in the same directory as the notebook (or adjust the path accordingly).

## Files included

*   `Predicting Breast Cancer.ipynb`: The main Jupyter Notebook containing all the executed code, visualizations, and modeling steps.
*   `cancer.csv`: The dataset used for training and evaluating the models.
