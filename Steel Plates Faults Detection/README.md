#Steel Plates Faults Detection

## Introduction
The prediction of steel plate faults can help prevent accidents that could harm humans. As the response variable is binary, our goal is to train several classification models to classify the type of fault in steel plates. We will compare the performance of different models to identify the best model for predicting faults.

## Dataset
This dataset comes from research conducted by Semeion, Research Center of Sciences of Communication. It consists of 1941 observations and includes 27 features describing the geometric shape of faults and 7 class labels indicating the type of fault.

## Data Analysis and Visualization


## Data Preprocessing
Separate the variables into Features (X) as input and Faults (y) as the output.
Data cleaning: Check and remove any missing values.
Data splitting: Split the data into a 70% training set and a 30% test set.
Data normalization: Apply Min-Max normalization and standardization for better model performance.
Oversampling: Handle imbalanced classes by oversampling the minority class.

## Model Selection - Classification Models


Justification:
The dataset consists of multiple categories.
The dataset includes labels.
⇒ We believe that using a regression model instead of a classification model would result in lower accuracy.
Methods

Four classification methods were used: K Nearest Neighbor, Logistic Regression, Random Forest, and XGBoost.
Principal Component Analysis (PCA) was used to reduce the dimensions to 19.
All approaches were implemented with and without PCA.

## Classification Methods
K Nearest Neighbor (k=3): A density-based classification algorithm that predicts groupings of individual data based on proximity.
⇒ Smaller k values result in smaller test errors.
Logistic Regression: A linear classification algorithm that assumes the class attribute is linear in the coefficients of the predicted attribute, which are used to predict the probability of an event occurring.
Random Forest (max_depth=20): A decision-tree-based classification algorithm consisting of many decision trees. In a random forest, a subset of features is randomly selected, and the best predictors are chosen.
⇒ Deeper max_depth values result in smaller test errors.
XGBoost (learning_rate=0.3): A decision-tree-based ensemble classification algorithm that uses a gradient-boosting framework.
⇒ The optimal learning rate is 0.3.

Classification Using PCA
Minimizes the dimensionality of a dataset with many correlated variables while preserving the variation present in the dataset.
Helps avoid overfitting in testing and training.
The feature vector of 10-20 principal components can represent the data.
PCA was used to reduce the dimensions to 19.

## Results - Comparison
The fault diagnosis performance of the models was evaluated using statistical accuracy.

Model without PCA:

Random Forest performed the best with an accuracy of 76.0%.
K Nearest Neighbor and XGBoost achieved accuracy above 70%.
Model with PCA:

Random Forest performed the best with an accuracy of 76.7%.
K Nearest Neighbor and XGBoost achieved accuracy above 70%.

## Conclusion
In this report, we trained four classification models to predict the type of faults in steel plates. Three of the models were learned from class, including K-Nearest Neighbor, Random Forest, and Logistic Regression. An additional model not covered in class, Extreme Gradient Boosting, was also used. We split the data into a training set and a test set. Dimension reduction was performed using PCA, reducing the number of predictors from 27 to 19. After comparing the models with and without PCA, we found that the Random Forest model with PCA performed the best, achieving the highest accuracy of 76.7%. We also observed that even without PCA, the Random Forest model still outperformed the other models.
