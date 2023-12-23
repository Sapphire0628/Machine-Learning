# Credit Card Approval Prediction

## 1. Introduction:

Credit cards are widely used for payments, but the manual processing of credit card applications is prone to errors and inefficiencies. To improve productivity and efficiency, machine learning-based credit card approval predictions have become valuable. With advancements in technology and the era of big data, machine learning plays a significant role in predictive analysis. Financial institutions and banks face the challenge of assessing risk factors when providing credit to customers. Machine learning tools can be used to identify low-risk customers and minimize the risk of credit defaults. In this study, we utilize individual information and applicant data to predict the likelihood of future credit card defaults. We conduct exploratory data analysis, compare supervised machine learning algorithms, extract key features for identifying "bad" clients, and select the best-performing algorithm for credit card approval predictions. The chosen algorithm achieves approximately 90% accuracy in prediction. This project highlights the use of machine learning in detecting credit risk and presents findings on customer credit risk assessment.

### 1.1 Dataset
The data was collected from the Kaggle Platform. Application_record.csv showed the credit card
application records and it contains around 430,000 rows & 18 features. Credit_record.csv show
monthly credit card account status respectively and it contains around 1,000,000 rows
& 3 features. 

### 1.2 Challenge

In this project, there are the following challenges:
- The dataset is **highly imbalanced**.
- The definition of **'good' or 'bad' is not given**. The target must be defined

### 1.3 Objective

Our achievement in this project is to:
- Determine the **important features** that affect the credit card approval result.
- Use predictors to **predict** the credit card approval result with high accuracy

## 2 Data Processing

### 2.1 Data Integration – defining target and merging

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

The target is determined by below logic:

<img src='./image/TargetDefinition.png' width='500'>

### 2.2 Data Cleaning

#### 2.2.1 Remove duplicate
> After duplicate removal by using Pandas, the data left 32713 rows.
#### 2.2.2 Filter unwanted outliers
> Handling ouliter using 99.7 rule(Make sure don't remove many information)
#### 2.2.3 Handle missing value
> One variable has 14% missing values, which is the categorical feature. The solution is to ignore missing values.

### 2.3 Data Wrangling

#### 2.3.1 One-hot encoding
> One-hot encoding is utilized to transform categorical data into separate columns in the dataset.
#### 2.3.2 Train-test splitting
> Train-test splitting is applied at a ratio of 7:3 to prevent overfitting.
#### 2.3.3 Oversampling
> SMOTE is employed to address imbalanced data. It's important to note that oversampling is performed after the train-test split to avoid the possibility of observations from the minority class in the training dataset appearing in the testing dataset. This ensures that the algorithm does not learn from similar instances and prevents any potential bias or cheating.

## Exploratory data analysis (EDA)

