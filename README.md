# Customer Churn Prediction

![Python](https://img.shields.io/badge/Python-3.x-blue)
![sklearn](https://img.shields.io/badge/scikit--learn-ML-orange)

Customer churn is one of the most costly problems facing banks and financial institutions. This project builds a machine learning model using a Random Forest Classifier to identify customers at risk of leaving, enabling early intervention and targeted retention strategies. The model achieves an accuracy of 86.6% on held-out test data.

Given a customer's credit score, account balance, activity status, and demographic information, can we predict whether they will exit the bank? The goal is to shift from reactive to proactive customer retention.

## About Dataset
*    Source: https://www.kaggle.com/datasets/shrutimechlearn/churn-modelling/data
*    10,000 rows, 14 columns
*    Target variable: Exited (1 = churned, 0 = stayed)

| Column          | Description                          |
|-----------------|--------------------------------------|
| CreditScore     | Customer's credit score              |
| Geography       | Country of the customer              |
| Gender          | Customer's gender                    |
| Age             | Customer's age                       |
| Tenure          | Years with the bank                  |
| Balance         | Account balance                      |
| NumOfProducts   | Number of bank products used         |
| HasCrCard       | Whether customer has a credit card   |
| IsActiveMember  | Whether customer is actively engaged |
| EstimatedSalary | Estimated annual salary              |
| Exited          | 1 = churned, 0 = stayed (target)     |

```
customer-churn-prediction/
├── data/
│   └── Churn_Modelling.csv
├── Churn_Model.ipynb
└── README.md
```

## Methodology
The dataset was cleaned by removing non-predictive identifier columns. Exploratory data analysis was conducted to understand churn patterns across age, geography, activity status, and salary. Categorical variables were encoded using Label Encoding and One-Hot Encoding. Features were scaled using StandardScaler before model training. A Random Forest Classifier was trained with class_weight='balanced' to handle the 80/20 class imbalance in the target variable. Model performance was evaluated using accuracy, precision, recall, and F1 score.

### Key Vizualizations
![Churn Distribution](Churn%20Distribution.png)

*Churn Distribution showing class imbalance, with approximately 80% of customers not churned (0) and 20% churned (1).*




![Churn Rate by Age](Churn%20Rate%20by%20Age.png)

*Churners are more likely to be older*


## Results
The model achieved an accuracy of 86.6% and an F1 score of 0.869 on the test set. Feature importance analysis identified Age, EstimatedSalary, and CreditScore as the strongest predictors of churn.

## Business Insights
*    Customers aged 45 and above churn at significantly higher rates. Targeted retention offers for this segment could reduce attrition meaningfully
*    Inactive members are nearly twice as likely to churn. Re-engagement campaigns represent a high-ROI intervention
*    German customers show the highest churn rate across all geographies. This is worth investigating regional service quality

## How to Run
```
git clone https://github.com/yourname/customer-churn-prediction
cd customer-churn-prediction
pip install -r requirements.txt
jupyter notebook
```

## Tools Used
Python, pandas, NumPy, scikit-learn, matplotlib, seaborn

## Author
Odelowo Eriolaoluwa

Github: https://github.com/Moyothon

Linkedin: https://www.linkedin.com/in/eriolaoluwa-odelowo-b08247249/

Email: eriolarabel@gmail.com
