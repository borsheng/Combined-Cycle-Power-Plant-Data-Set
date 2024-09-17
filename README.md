# Combined Cycle Power Plant Data Set

## Project Overview

This project involves exploring and analyzing a dataset from a Combined Cycle Power Plant (CCPP) using various regression techniques, including linear regression, polynomial regression, and K-Nearest Neighbor (KNN) regression. The dataset contains hourly average ambient variables that impact the net hourly electrical energy output (EP) of the power plant. The project aims to predict EP using these predictors and compare the performance of different regression models.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Regression Analysis](#regression-analysis)
- [KNN Regression](#knn-regression)
- [How to Run](#how-to-run)
- [Results](#results)
- [License](#license)

## Dataset

The dataset contains 9,568 data points collected over six years (2006-2011) from a Combined Cycle Power Plant. The plant operates at full load, and the dataset includes the following features:

- **Temperature (T)**: Ambient temperature
- **Ambient Pressure (AP)**: Atmospheric pressure
- **Relative Humidity (RH)**: Ambient relative humidity
- **Exhaust Vacuum (V)**: Vacuum pressure
- **Energy Output (EP)**: Net hourly electrical energy output of the power plant (dependent variable)

The dataset is provided in both `.ods` and `.xlsx` formats, shuffled into five different versions. For this analysis, we work with **Sheet 1**.

## Exploratory Data Analysis

1. **Pairwise Scatterplots**:
   - Scatterplots were generated for each pair of features, including the predictors and the dependent variable (EP).
   - Observations: [Add findings based on scatterplot analysis, such as any linear/non-linear relationships or outliers.]

2. **Summary Statistics**:
   - For each feature, the following statistics were computed:
     - Mean
     - Median
     - Range
     - First and third quartiles
     - Interquartile range
   - These statistics provide a clear overview of the data distribution.

## Regression Analysis

1. **Simple Linear Regression**:
   - Each predictor (T, AP, RH, V) was regressed against the response (EP) independently.
   - **Results**: [Add findings about which predictors had statistically significant associations with EP.]
   - Plots were created to visualize the relationships, including potential outliers that were identified and considered for removal.

2. **Multiple Linear Regression**:
   - A multiple regression model was fitted using all predictors to predict the response (EP).
   - **Null Hypothesis Test**: For each predictor, we tested if \(\beta_j = 0\). [Add results regarding which predictors' null hypotheses could be rejected.]

3. **Comparison of Simple vs. Multiple Regression**:
   - A plot was generated comparing the coefficients of the univariate and multiple regression models. This comparison illustrates how the inclusion of multiple variables influences the coefficient estimates.

4. **Nonlinear Regression**:
   - Polynomial regression models were fitted for each predictor to explore potential nonlinear relationships.
   - **Results**: [Add findings about any significant nonlinear associations.]

5. **Interaction Terms**:
   - Pairwise interaction terms were added to the model to check for significant interactions between predictors.
   - **Results**: [Add findings regarding the significance of interaction terms.]

6. **Model Improvement**:
   - Regression models with interaction terms and quadratic nonlinearities were trained on 70% of the data, with insignificant variables removed based on p-values.
   - **Train and Test MSEs**: The models were evaluated on the remaining 30% of the data, and both train and test Mean Squared Errors (MSEs) were reported.

## KNN Regression

1. **K-Nearest Neighbors Regression**:
   - KNN regression was performed using both normalized and raw features. The optimal value of k was determined by testing values in the range \(k \in \{1, 2, \ldots, 100\}\).
   - Train and test errors were plotted against \(1/k\), and the best k value was selected.
   
2. **Comparison to Linear Regression**:
   - The results of KNN regression were compared to the best linear regression model based on test errors.
   - **Findings**: [Add analysis comparing the performance of KNN regression and linear regression.]

## How to Run

### Requirements

- Python 3.x
- Jupyter Notebook
- Required Python libraries (can be installed via `pip`):
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`

### Instructions

1. Clone the repository and navigate to the project folder.
2. Open the Jupyter Notebook (`Huang_Bor-Sheng.ipynb`).
3. Run the notebook cells to execute the analysis and view results.

## Results

- **Best Linear Regression Model**: [Add the predictors and their coefficients from the best linear regression model.]
- **KNN Regression**: [Add the optimal k value and corresponding test error.]
- **Train and Test MSEs**: [Add the MSEs for both the linear and KNN models.]

## License

This project is intended for academic purposes and is based on the DSCI 552 course material.

