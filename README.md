# AandBtesting_covariate_cs203

## Project Overview

This project involves two main tasks:

1. **A/B Testing and Statistical Analysis**:  
   We perform A/B testing on user data to determine whether there is a statistically significant difference between two groups based on ad position.
   
2. **Covariate Shift Detection**:  
   We use air quality data to detect covariate shifts between training and test datasets using the Kolmogorov–Smirnov test.

## Task Breakdown

### Part 1: **A/B Testing and Statistical Analysis**  
- **Objective**: Perform A/B testing on ad data to check if ad position influences user clicks.
- **Approach**: 
  - Clean the dataset by handling missing values (removing those rows) and converting categorical variables.
  - Perform an independent two-sample Z-test using the proportions of clicks in Group A (Top ad position) and Group B (Side ad position).
- **Notebook**: [notebook1.ipynb](notebook1.ipynb)

### Part 2: **Covariate Shift Detection**  
- **Objective**: Detect covariate shift using air quality data by comparing `NO2(GT)` distributions in training and test datasets.
- **Approach**: 
  - Load the datasets and clean the data (handle numeric conversion).
  - Use the Kolmogorov–Smirnov (KS) test to compare the `NO2(GT)` column between the training set and two test datasets.
  - Identify any covariate shift between the datasets based on the KS test results.
- **Notebook**: [notebook2.ipynb](notebook2.ipynb)

## Key Results

### Part 1: A/B Testing
- **KS Test Result**: The p-value for Group A vs. Group B was used to assess statistical significance, and the findings helped determine whether ad position influences user clicks. We failed to reject the null hypothesis. 

### Part 2: Covariate Shift Detection
- **KS Test Result**: 
  - **test_1 vs train**: No significant covariate shift detected (p-value: 0.972).
  - **test_2 vs train**: Significant covariate shift detected (p-value: ~0).

## How to Use the Notebooks

1. Clone or download the project.
2. Open the notebooks `notebook1.ipynb` and `notebook2.ipynb` in Jupyter or any compatible environment.
3. Ensure the necessary libraries (pandas, scipy, etc.) are installed.
4. Run each cell to reproduce the results.

## Requirements

- pandas
- scipy
- numpy
- stats
  
