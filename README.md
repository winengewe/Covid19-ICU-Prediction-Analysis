# COVID-19 ICU Prediction Analysis 🏥📊

## Overview
This repository contains a Data Science assessment project completed for the **GP8R46 NPA Data Science** course. The goal of this project is to act as a Data Scientist for the Scottish Government to assist in the COVID-19 pandemic response.

By analyzing daily published statistics, this project aims to predict the number of patients requiring Intensive Care Units (ICU), enabling the NHS to allocate resources effectively.

## 📂 Dataset
The analysis uses a distilled version of open license relational data from the [Scottish Government](https://www.gov.scot/publications/coronavirus-covid-19-trends-in-daily-data/).
* **Data Source:** `covid19.csv`
* **Key Features:** Dates, First/Second Doses, Hospital Admissions, Positive Tests, and ICU numbers.

## 🛠️ Technologies Used
* **Python** 🐍
* **Pandas** (Data Manipulation)
* **NumPy** (Numerical Analysis)
* **Matplotlib & Seaborn** (Data Visualization)
* **Scikit-Learn** (Machine Learning)

## 🔍 Key Analysis Steps
1.  **Data Cleaning:** Handling missing values and structuring the dataset for analysis.
2.  **Exploratory Data Analysis (EDA):**
    * Statistical summary of the data.
    * Visualizing relationships between variables (e.g., *Second Dose vs. ICU*, *Positive Tests vs. ICU*).
    * Correlation analysis to identify key predictors.
3.  **Feature Selection:** Identified `positive_tests` as the feature most strongly correlated with ICU admissions.
4.  **Machine Learning:**
    * Splitting data into Training (90%) and Testing (10%) sets.
    * Training a **Linear Regression** model.
    * Evaluating model performance using $R^2$ scores.

## 📈 Model Performance
The project compares two modeling approaches to predict ICU numbers:

### 1. Linear Regression
* **Training Score:** ~91.4%
* **Testing Score:** ~87.8%
* *Observation:* The model provides a decent baseline but struggles with complex patterns.

### 2. Random Forest (Comparison)
* **Training Score:** ~99.0%
* **Testing Score:** ~94.7%
* *Conclusion:* The Random Forest model outperformed Linear Regression. It was able to capture non-linear relationships in the data (e.g., high vaccination rates dampening the effect of positive cases on ICU admissions).

## 🚀 How to Run
1.  Clone this repository.
2.  Ensure you have the required libraries installed:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```
3.  Open the Jupyter Notebook `Covid19_ICU_Prediction_Analysis.ipynb` to view the analysis and code.

## 📜 Assessment Context
This evidence was produced for the **Combined J2G246 Data Science, J2HN46 Data Citizenship & J2G646 Machine Learning Assessment**.
