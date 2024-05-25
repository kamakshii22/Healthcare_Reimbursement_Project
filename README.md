<h1 align="center">
  Predicting Future Healthcare Reimbursements
</h1>
<div align="center">
  <h4>Aurthor: <a href="https://www.linkedin.com/in/kamakshisharma22">Kamakshi Sharma</a></h4>
</div>

This repository contains an analysis focused on predicting future Medicare reimbursements using various machine learning techniques. The project's goal is to assist healthcare providers and policymakers in making strategic decisions and improving financial planning through accurate predictions.

## Data Description

- **Datasets:** Comprehensive information on Medicare enrollees, reimbursement amounts, healthcare services, and demographic factors.
- **df_state:** State-level data & **df_county:** County-level data.

## Approach
Extensive **Data Cleaning and Preprocessing** was done to ensure accurate analysis and modeling. This included renaming columns for clarity, removing redundant rows, and handling null values. We converted inappropriate data types to their correct formats and imputed missing values using state-level data to fill county-level gaps, ensuring data completeness and consistency.<br>

Performed **Exploratory Data Analysis (EDA)** on both state and county datasets to understand feature distributions and correlations. This included visualizing data to identify patterns and relationships that affect Medicare reimbursements, and addressing any data quality issues discovered during this process.<br>

Does **Feature Engineering** and refined existing ones to enhance model performance. This step also involved mapping and imputing missing values from state-level data for county-level analysis.<br>

For **Model Building** implemented three regression models:
  - **Linear Regression**
  - **Random Forest Regression**
  - **Gradient Boosting Regression** <br>
  
The data was split into training and testing sets (80/20 split). We performed target encoding for categorical variables and normalized features using Min-Max Scaling.<br>

Done **Model Evaluation** using metrics Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE) & R-squared (R²) Score. 

**Model Comparison**

| Model                       | MAE    | MSE       | RMSE   | R²     |
|-----------------------------|--------|-----------|--------|--------|
| Linear Regression           | 10.81  | 1211.94   | 34.81  | 0.999  |
| Random Forest Regression    | 250.75 | 158751.21 | 398.44 | 0.923  |
| Gradient Boosting Regression| 202.24 | 100131.45 | 316.43 | 0.951  |

### Best Model Selection <br>
**Linear Regression** emerged as the best model for predicting Medicare reimbursements, demonstrating the highest R-squared value and the lowest error metrics.

## Feature Importance Analysis

We analyzed the coefficients of the linear regression model to identify key factors influencing Medicare reimbursements. The **top influential features** are:
  - Total Medicare Reimbursements per Enrollee (Ttl_Mcr_Reim_P_E_14_ASRA)
  - Hospital Skilled Nursing Reimbursement (Hosp_SN_Reim_P_E_14_P_ASRA)
  - Outpatient Facility Reimbursement (Outp_Fac_Reim_P_E_14_P_ASRA)
  - Physician Reimbursement (Phys_Reim_P_E_14_P_ASRA)
  - Home Health Agency Reimbursement (HHA_Reim_P_E_14_P_ASRA)

## Conclusion

The project successfully developed a predictive model for Medicare reimbursements, with **Linear Regression** providing the best performance. Key factors influencing costs were identified, offering valuable insights for healthcare providers and policymakers to optimize resource allocation and financial planning.

## GitHub Files

- Jupyter Notebook: [Predicting Future Healthcare Reimbursements](https://github.com/kamakshii22/Healthcare_Reimbursement_Project/blob/main/Healthcare_Reimbursement_Project.ipynb)
- Report: [Healthcare Reimbursements Prediction Report](https://github.com/yourusername/healthcare-reimbursements/blob/main/Healthcare_Reimbursements_Prediction_Report.pdf)
