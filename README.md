<h1 align="center"> Telecom Churn Prediction Project</h1>

This project focuses on predicting customer churn for a telecommunications company using Machine Learning techniques.
*The in-depth Python code explanation is available in [this](https://github.com/vitortbarboza/Telecom_Churn/blob/main/Telecom_Churn.ipynb) Jupyter Notebook.*

# 1. **Introduction**

Customer churn, the rate at which customers leave a service, is a critical metric for businesses. In this project, we aim to analyze and predict churn for a telecommunications company. By understanding the factors influencing churn and employing Machine Learning models, we strive to assist the company in retaining customers.

# 2. **Objective**

The primary objectives of this project are as follows:

- Analyze and understand customer churn patterns.
- Develop Machine Learning models to predict customer churn.
- Provide insights and recommendations for reducing churn rates.

# 3. **Technologies**
The project leverages the following technologies:

- Python
- Machine Learning Libraries (e.g., scikit-learn, XGBoost, CatBoost)
- Data Analysis and Visualization Libraries (e.g., Pandas, Matplotlib, Seaborn)
- Jupyter Notebook

# 4. **Methodology**

- Data Preprocessing: Cleaning, handling missing values, encoding categorical variables, etc.
- Exploratory Data Analysis: Understanding data patterns and relationships.
- Feature Engineering: Creating new features or modifying existing ones for model training.
- Model Selection: Trying various ML models and selecting the best-performing one.
- Model Evaluation: Assessing model performance using appropriate metrics.

# 5. **Principal Insights**

- Gender does not have a significant impact on churn.
- Elderly customers have a higher cancellation rate compared to non-elderly customers.
- Single customers are more likely to cancel the service.
- Customers without dependents are more likely to cancel the service.
- There is not much difference in the cancellation rate between people who have the phone service and those who do not.
- There is a high cancellation rate among customers using fiber optic service, suggesting dissatisfaction with this service.
- Regarding online security, it is noticed that customers who do not have this service have a high cancellation rate.
- Customers without OnlineBackup and DeviceProtection have a high cancellation rate.
- Customers without TechSupport have a high cancellation rate.
- More than half of the contracts are month-to-month, and these account for the vast majority of canceled subscriptions.
- Customers with PaperlessBilling are more likely to churn.
- Customers using Electronic Check are more likely to churn.

# 6. **Model Evaluation**
In this section, we present the evaluation of different machine learning models and their respective financial implications in addressing customer churn for the telecommunications company.

## 6.1. **Models Explored**

We experimented with the following models:
- Random Forest Classifier
- Logistic Regression
- XGBoost Classifier
- CatBoost Classifier

## 6.2. **Evaluation Metrics**
We used the following evaluation metrics to assess model performance:

- Accuracy: Overall accuracy of the model in predicting churn.
- Precision: Proportion of true positive predictions among all positive predictions.
- Recall: Proportion of true positive predictions among all actual positives.
- F1 Score: Harmonic mean of precision and recall.
- ROC AUC Score: Area under the Receiver Operating Characteristic curve.
- Financial Return: Estimated financial return based on model predictions.

## 6.3. **Financial Implications**
The estimated financial return is based on the model's predictive ability to reduce churn. The values provided are approximate and subject to variations based on real-world implementation and other influencing factors.
By evaluating recall and precision from Beanchmarking model, we found that the model correctly identified 58.84% of actual churn cases while correctly predicting 62.86% of predicted churn cases.
Assuming a promotion of **"Get a 25% discount on your monthly recharge for the next 6 months!"** is offered to potentially churned customers and that this promotion would retain these customers for an additional 6 months, we'll calculate the financial return considering the following:
- Gained revenue by retaining customers who would churn.
- Missed revenue due to offering the promotion to customers who wouldn't actually churn.

The total revenue gained from retaining customers who would churn is: R$87964.88
The total revenue lost due to the churn of customers that our model didn't predict is: R$63448.43
The total revenue missed by offering the promotion to customers who wouldn't churn is: R$21149.47

With this model in production, we would have an estimated profit of **R$3,336.97**.

Next, we will estimate the models by adjusting the class_weight to assess the financial impact of this adjustment. After the adjustments, We achieved a recall of 79,48% in the Logistic Regression model after Bayesian hyperparameter optimization. And we performed the same calculation to estimate the financial return.

he total revenue gained from retaining customers who would churn is: R$125,245.80
The total revenue lost due to the churn of customers that our model didn't predict is: R$26,167.50
The total revenue missed by offering the promotion to customers who wouldn't churn is: R$8,722.50

With this model in production, we would have an estimated profit of **$90,355.80**. A significantly higher profit compared to the first model.

# 7. **Suggestions for Operational Improvements**
- We need to work on measures to reduce the cancellation rate among elderly customers, as this demographic is willing to pay more for the service.
-  We noticed that the vast majority of contracts are month-to-month and these are the main contributors to churn. Our proposal is to create quarterly or semi-annual subscriptions at an affordable price. In these new plans, we should offer the following services: OnlineSecurity, OnlineBackup, DeviceProtection, and TechSupport. Our goal with these plans is to try to create a longer-lasting relationship with the customer, allowing them enough time to explore all our available services. According to our analysis, as the customer becomes more familiar with the service, the chances of customer retention increase.
- We noticed that many customers are not satisfied with the fiber optic internet. Therefore, we should invest in infrastructure to improve this service.
- We suggest discontinuing the use of Electronic Check for payment purposes due to its high cancellation rate and focusing exclusively on Bank Transfer and Credit Card.
- Improving the TechSupport service is essential, as we found that this variable is one of the most important in determining whether the user will cancel the service.
