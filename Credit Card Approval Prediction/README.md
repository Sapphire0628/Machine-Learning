# Credit Card Approval Prediction

## Introduction:

Credit cards are widely used for payments, but the manual processing of credit card applications is prone to errors and inefficiencies. To improve productivity and efficiency, machine learning-based credit card approval predictions have become valuable. With advancements in technology and the era of big data, machine learning plays a significant role in predictive analysis. Financial institutions and banks face the challenge of assessing risk factors when providing credit to customers. Machine learning tools can be used to identify low-risk customers and minimize the risk of credit defaults. In this study, we utilize individual information and applicant data to predict the likelihood of future credit card defaults. We conduct exploratory data analysis, compare supervised machine learning algorithms, extract key features for identifying "bad" clients, and select the best-performing algorithm for credit card approval predictions. The chosen algorithm achieves approximately 90% accuracy in prediction. This project highlights the use of machine learning in detecting credit risk and presents findings on customer credit risk assessment.

### Dataset
The data was collected from the Kaggle Platform. Application_record.csv showed the credit card
application records and it contains around 430,000 rows & 18 features. Credit_record.csv show
monthly credit card account status respectively and it contains around 1,000,000 rows
& 3 features. 

### Challenge

In this project, there are the following challenges:
- The dataset is **highly imbalanced**.
- The definition of **'good' or 'bad' is not given**. The target must be defined

### Objective

Our achievement in this project is to:
- Determine the **important features** that affect the credit card approval result.
- Use predictors to **predict** the credit card approval result with high accuracy

## Data Processing

### Data Integration – defining target and merging

In the dataset, due payment days can be observed. Assume that a person is considered **a ‘Bad’ client if he has unpaid payments for more than 60 days**. Status is defined by:

| Status  | Meaning |
| ------------- | ------------- |
| 0  | 1-29 days past due  |
| 1  | 30-59 days past due  |
| 2  | 60-89 days overdue  |
| 3  | 90-119 days overdue  |
| 4  | 120-149 days overdue  |
| 5  | Overdue or bad debts, write-offs for more than 150 days  |
| C  | Paid off that month  |
| X  | No loan for the month  |
