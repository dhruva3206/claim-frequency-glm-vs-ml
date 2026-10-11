# Claim Frequency Prediction: Actuarial GLM vs Machine Learning

## Overview

This project explores the application of traditional actuarial modelling and machine learning techniques to predict motor insurance claim frequency using the French Motor Third-Party Liability (MTPL) dataset.

The primary objective is to compare a traditional actuarial Generalized Linear Model (GLM) with machine learning models and evaluate their predictive performance.

## Objectives

* Perform data cleaning and exploratory data analysis.
* Apply actuarial concepts to insurance claim frequency modelling.
* Develop a Poisson GLM as a traditional actuarial benchmark.
* Implement machine learning models for claim frequency prediction.
* Compare model performance using appropriate evaluation metrics.
* Identify limitations and opportunities for further improvement.

## Dataset

The project uses the French Motor Third-Party Liability Claims (`freMTPL2`) dataset, which contains motor insurance policy information, including claim counts, exposure, and policyholder and vehicle characteristics.

**Dataset source:** [French Motor Third-Party Liability Claims — Kaggle](https://www.kaggle.com/datasets/karansarpal/fremtpl2-french-motor-tpl-insurance-claims)

## Methodology

### 1. Data Preparation and Exploratory Analysis

* Examined the dataset structure and variable distributions.
* Investigated missing values and relevant risk characteristics.
* Prepared the data for modelling.

### 2. Actuarial Modelling

* Developed a Poisson GLM for claim frequency prediction.
* Incorporated exposure through a log-exposure offset to account for differences in policy exposure.

### 3. Machine Learning

* Developed Decision Tree and Random Forest models.
* Incorporated exposure into the relevant model training approach using sample weighting where applicable.

### 4. Model Evaluation

* Evaluated the models using the selected performance metrics.
* Compared traditional actuarial modelling with machine learning approaches.

## Results and Interpretation

The models were compared to investigate the differences between traditional actuarial and machine learning approaches to claim frequency prediction.

**Key findings:** 
* There isn't always a single model performing the best across all metrics
* The Poisson GLM achieved the lowest MAE, Random Forest performed best in terms of RMSE and Mean Poisson Deviance.
* The Random Forest outperformed the single Decision Tree across all three evaluation metrics.
* Further improvements could be explored using trial and error, such as using Negative Binomial GLM or
tuning parameters of existing ML algorithms or trying new algorithms altogether such as Boosting

<img width="512" height="108" alt="image" src="https://github.com/user-attachments/assets/f7940875-c6ef-4cb9-95e7-3cfeaec8b4fe" />


## Limitations

* The analysis is based on a single dataset and may not represent all insurance portfolios.
* Model performance depends on data quality, feature selection, and modelling assumptions.
* Machine learning models may be less interpretable than traditional actuarial GLMs.
* Further improvements could be explored using Negative Binomial GLMs, gradient boosting, and hyperparameter tuning with GridSearchCV.

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Statsmodels
* Matplotlib and Seaborn
* Jupyter Notebook

## Future Improvements

* Explore alternative actuarial count models, including Negative Binomial GLMs.
* Tune model hyperparameters using GridSearchCV.
* Investigate gradient boosting algorithms.
* Evaluate additional performance measures and model calibration.
* Explore more robust exposure-adjusted modelling approaches.

## How to Run

1. Clone or download this repository.
2. Install the required Python libraries.
3. Download the dataset from the source provided above.
4. Place the dataset files in the locations specified in the notebook.
5. Open the Jupyter Notebook and execute the cells in order.

## Acknowledgments & Data Source

This project utilizes the **French Motor Third-Party Liability Claims (`freMTPL2`)** dataset.

* **Dataset:** [French Motor Third-Party Liability Claims — Kaggle](https://www.kaggle.com/datasets/karansarpal/fremtpl2-french-motor-tpl-insurance-claims)
* **Dataset curator/uploader:** [Karan Sarpal](https://www.kaggle.com/karansarpal)

