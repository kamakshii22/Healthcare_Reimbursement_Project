<h1 align="center">
  Predicting Future Healthcare Reimbursements
</h1>
<div align="center">
  <h4>Author: <a href="https://www.linkedin.com/in/yourprofile">Your Name</a></h4>
</div>

This repository contains an analysis focused on predicting future Medicare reimbursements using various machine learning techniques. The project's goal is to assist healthcare providers and policymakers in making strategic decisions and improving financial planning through accurate predictions.

## Data Description

- **Datasets:** Comprehensive information on Medicare enrollees, reimbursement amounts, healthcare services, and demographic factors.
- **df_state:** State-level data including 52 rows and 17 columns.
- **df_county:** County-level data with 3144 rows and 17 columns.

## Approach

1. **Data Cleaning and Preprocessing**
    - Renamed columns for clarity.
    - Removed redundant rows and handled null values.
    - Converted inappropriate data types to ensure accurate analysis.
    - Imputed missing values using state-level data to fill county-level gaps.

2. **Exploratory Data Analysis (EDA)**
    - Analyzed data distribution, identified data quality issues, and addressed them.
    - Conducted EDA on both state and county datasets to understand feature distributions and correlations.
    - Visualized data to identify patterns and relationships affecting Medicare reimbursements.

3. **Feature Engineering**
    - Created new features and refined existing ones to enhance model performance.
    - Mapped and imputed missing values from state-level data for county-level analysis.

4. **Model Building**
    - Implemented three regression models:
        - **Linear Regression**
        - **Random Forest Regression**
        - **Gradient Boosting Regression**
    - Split the data into training and testing sets (80/20 split).
    - Performed target encoding for categorical variables and normalized features using Min-Max Scaling.

5. **Model Evaluation**
    - Evaluated models using metrics:
        - Mean Absolute Error (MAE)
        - Mean Squared Error (MSE)
        - Root Mean Squared Error (RMSE)
        - R-squared (R²) Score

6. **Model Comparison**

| Model                       | MAE    | MSE       | RMSE   | R²     |
|-----------------------------|--------|-----------|--------|--------|
| Linear Regression           | 10.81  | 1211.94   | 34.81  | 0.999  |
| Random Forest Regression    | 250.75 | 158751.21 | 398.44 | 0.923  |
| Gradient Boosting Regression| 202.24 | 100131.45 | 316.43 | 0.951  |

### Best Model Selection
- **Linear Regression** was selected as the best model due to its highest R-squared value (0.999) and lowest error metrics (MAE: 10.81, RMSE: 34.81).

## Feature Importance Analysis

- Analyzed the coefficients of the linear regression model to identify key factors influencing Medicare reimbursements.
- **Top Influential Features:**
    - Total Medicare Reimbursements per Enrollee (Ttl_Mcr_Reim_P_E_14_ASRA)
    - Hospital Skilled Nursing Reimbursement (Hosp_SN_Reim_P_E_14_P_ASRA)
    - Outpatient Facility Reimbursement (Outp_Fac_Reim_P_E_14_P_ASRA)
    - Physician Reimbursement (Phys_Reim_P_E_14_P_ASRA)
    - Home Health Agency Reimbursement (HHA_Reim_P_E_14_P_ASRA)

## Conclusion

The project successfully developed a predictive model for Medicare reimbursements, with **Linear Regression** providing the best performance. Key factors influencing costs were identified, offering valuable insights for healthcare providers and policymakers to optimize resource allocation and financial planning.

## GitHub Files

- Jupyter Notebook: [Predicting Future Healthcare Reimbursements](https://github.com/yourusername/healthcare-reimbursements/blob/main/Predicting_Future_Healthcare_Reimbursements.ipynb)
- Report: [Healthcare Reimbursements Prediction Report](https://github.com/yourusername/healthcare-reimbursements/blob/main/Healthcare_Reimbursements_Prediction_Report.pdf)
