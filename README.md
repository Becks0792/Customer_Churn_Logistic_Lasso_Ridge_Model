# Telco Customer Churn Data Analysis & Predictive Model

**Project Overview**
This project analyzes customer churn for a fictional Telco company that offers home phone and internet services. Churn is defined as the percentage of customers who stop using the company's services within a specific timeframe. Understanding and predicting churn is crucial for retaining customers and minimizing revenue loss.

**Dataset Description**
The dataset contains information on 7,043 customers from California, detailing their demographics, account information, and the services they have subscribed to, such as internet, security, and streaming options.

**Objectives**
- Identify key factors that predict customer churn.
- Develop a predictive model to forecast the likelihood of a customer leaving, enabling targeted customer retention strategies.
  
**Tools Used**
R Programming: For data manipulation, statistical testing, and modeling.
Libraries: ggplot2, dplyr, caret, glmnet, among others, for data visualization and machine learning.

**Methodology**
1. Data Cleaning
2. Exploratory Data Analysis (EDA)
3. Statistical Testing - Chi-Square & ANOVA
4. Predictive Modeling

**Models Built :**
- **Logistic Regression:** Employed as a baseline model using identified significant predictors. It offered an initial insight with an AUC of 0.8351, demonstrating reasonable predictive power.
- **Lasso Regression (L1 Regularization):** Applied to reduce feature complexity by penalizing the absolute size of the coefficients, leading to some coefficients being zeroed out. This model simplified the predictive process without substantial loss in performance, achieving an AUC of 0.844.
- **Ridge Regression (L2 Regularization):** Used to address multicollinearity among predictors by penalizing the square of the coefficients. It slightly improved model stability but provided similar accuracy and complexity metrics as the Lasso, with an AUC of 0.84.
- **Stepwise Regression:** Conducted to refine model accuracy through a sequential selection of significant predictors. This method yielded an AUC of 0.8439, slightly less effective than Lasso in terms of model simplicity.

**Model Selection**
The Lasso Regression was chosen as the optimal model due to its effective balance between model complexity and predictive accuracy. It successfully eliminated irrelevant features, reducing overfitting while maintaining a high AUC, making it the best tool for operational implementation in customer retention strategies.

**Key Findings**
- Services like online security and tech support significantly reduce churn probability.
- Customers with fiber optic internet service or month-to-month contracts are more likely to churn.
- Higher monthly charges and lower tenure increase the likelihood of churn.

**Implementation**
**Model Deployment:** The model can be deployed in a real-time prediction system where it can score customer records as they are updated, providing ongoing insights into potential churn risks.

**Usage Scenarios:** This model can assist in targeting customers with high churn probability through tailored retention programs, personalized offers, and proactive customer service initiatives to improve loyalty and reduce turnover.
   
