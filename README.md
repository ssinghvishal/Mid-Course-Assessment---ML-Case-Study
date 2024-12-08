# Model Comparison for Classification Problem
This project demonstrates the implementation, evaluation, and comparison of three popular classification models: Logistic Regression, Decision Tree, and Random Forest. The goal is to predict the target variable using these models and evaluate their performance based on metrics such as ROC-AUC, Accuracy, Precision, Recall, and F1 Score.

## Project Overview
The project involves the following steps:

### Data Preprocessing and Splitting:

Data is preprocessed and split into training and testing sets using SMOTE (Synthetic Minority Over-sampling Technique) to handle class imbalance.
Model Implementation:

### Logistic Regression: A linear model for binary classification.
### Decision Tree: A non-linear model that splits the data based on feature values.
### Random Forest: An ensemble learning method that combines multiple decision trees to improve performance.
## Model Tuning:

### Hyperparameter Tuning: The models, especially the Decision Tree and Random Forest, are tuned using GridSearchCV to find the best hyperparameters.
Cross-Validation: 5-fold cross-validation is used to evaluate the performance of the models.
Performance Evaluation:

### ROC-AUC: A metric used to evaluate the ability of the model to distinguish between classes.
Precision, Recall, and F1 Score: These metrics are used to assess the performance in terms of false positives and false negatives.
### Confusion Matrix: Visualizes the number of correct and incorrect predictions.
Model Comparison: A final comparison of all models is made based on the above evaluation metrics.

## Requirements
To run this project, the following Python libraries are required:

numpy
pandas
scikit-learn
matplotlib
seaborn
imbalanced-learn


## Model Evaluation Results
### 1. Logistic Regression
ROC_AUC: 0.790943
Accuracy: 0.725943
Precision: 0.721872
Recall: 0.735055
F1 Score: 0.728404
### 2. Decision Tree (Before Hyperparameter Tuning)
ROC_AUC: 0.737564
Accuracy: 0.567088
Precision: 0.585860
Recall: 0.457555
F1 Score: 0.513819
After Hyperparameter Tuning:

Best Parameters:
Criterion: gini
Max Depth: 9
Min Samples Split: 10
Max Features: None
Splitter: best
ROC_AUC (Tuned): 0.8036479378854811
### 3. Random Forest (Before Hyperparameter Tuning)
ROC_AUC: 0.902745
Accuracy: 0.636993
Precision: 0.878251
Recall: 0.318020
F1 Score: 0.466953
After Hyperparameter Tuning:

Best Parameters:
Max Depth: 40
N Estimators: 300
ROC_AUC (Tuned): 0.9057658962489562
## Key Insights:
Logistic Regression performs well overall with a good balance of precision and recall, making it a solid choice for this classification task.
Decision Tree struggles before tuning, with lower performance metrics. However, after hyperparameter tuning, its performance improves but still lags behind Logistic Regression in terms of overall accuracy and F1 Score.
Random Forest has the highest precision but struggles with recall. Its conservative nature in predicting positives results in a high number of false negatives, affecting the recall and F1 Score.
### Model Visualizations
1. Confusion Matrix:
The confusion matrices for all models are plotted to visualize the number of true positives, false positives, true negatives, and false negatives.

2. ROC-AUC Curve:
ROC curves for all three models are plotted to evaluate their ability to distinguish between the positive and negative classes.

3. Precision-Recall Curve:
Precision-Recall curves are plotted to evaluate the trade-off between precision and recall for each model.

## Conclusion
Logistic Regression emerges as the best overall model, with the highest accuracy, recall, and F1 Score, making it a reliable choice for balanced performance.
Random Forest is the most precise model but has a lower recall due to its tendency to classify more negative cases, which results in many false negatives.
Decision Tree, despite improvements after tuning, remains the least effective model compared to Logistic Regression and Random Forest in this case.
Future Work
Further tuning of the models could improve performance, especially for Decision Trees and Random Forests.
Exploring other classification models, such as Support Vector Machines or Gradient Boosting, could yield better results.
Implementing feature selection techniques might help improve model performance by removing irrelevant or redundant features.
