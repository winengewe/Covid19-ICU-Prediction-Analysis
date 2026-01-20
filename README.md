# COVID-19 ICU Admission Prediction 🏥📊

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1_yK--iyyCTWcDiw7YvDsgpkhbKSzw9-p?usp=sharing)

## 📌 Overview
This project is part of the **GP8R46 NPA Data Science** assessment. Acting as a Data Scientist for the Scottish Government, the goal of this analysis is to assist the NHS in effectively allocating resources during the pandemic. 

By analyzing daily published statistics, this notebook builds machine learning models to predict the number of patients requiring Intensive Care Unit (ICU) support based on other key indicators like positive test results.

## 📂 Dataset
The analysis uses the **Covid19 dataset**, which is distilled from open license relational data provided by the [Scottish Government](https://www.gov.scot/publications/coronavirus-covid-19-trends-in-daily-data/).
- **Input Features:** Daily positive tests, hospital admissions, vaccination doses (first/second).
- **Target Variable:** Number of patients in ICU.

## 🚀 Key Features & Methodology
1. **Data Cleaning:** Handling missing values and preparing the dataframe for analysis.
2. **Exploratory Data Analysis (EDA):** - Statistical summaries.
   - Correlation matrices to identify relationships between features.
   - Visualizations (Scatter plots) to observe trends between `positive_tests`, `second_dose`, and `icu`.
3. **Feature Selection:** Identifying `positive_tests` as the primary predictor for the regression models.
4. **Machine Learning Models:**
   - **Linear Regression:** A baseline model to establish linear relationships.
   - **Random Forest:** An ensemble method used to capture complex, non-linear patterns.
5. **Evaluation:** Comparing models based on training and testing scores ($R^2$ accuracy) to determine the best predictor for unseen data.

## 📊 Results
- The analysis highlights that **'positive_tests'** is highly correlated with ICU admissions.
- The **Random Forest model** outperformed Linear Regression, demonstrating better accuracy on both training and testing sets. It effectively handled non-linear relationships, such as the "dampening" effect of vaccinations on ICU numbers.

## 🛠️ Technologies Used
- **Python**
- **Pandas & NumPy** (Data Manipulation)
- **Matplotlib & Seaborn** (Data Visualization)
- **Scikit-Learn** (Machine Learning)

## 💻 How to Run
1. Open the notebook in [Google Colab](https://colab.research.google.com/).
2. Upload the `covid19.csv` dataset to your Colab session storage or mount your Google Drive.
3. Run the cells sequentially to reproduce the analysis and model predictions.

---
*This assessment covers Learning Outcomes for J2G246 Data Science, J2HN46 Data Citizenship, and J2G646 Machine Learning.*
