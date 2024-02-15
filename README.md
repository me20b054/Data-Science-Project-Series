Documentation for Breast Cancer Prediction:

In the given dataset of 570 rows and 30 columns has no null values
Converted categorical labels Malignant(M) to 1 and Begnin to 0
dropped the id columns as it has no contribution in final perdiction

visualised correlation between features using confusion_matrix of correlations between the features 
and recorded the features with correlation > 98%
radius_mean,perimeter_mean - 100%
radius_mean,area_mean - 99%
perimeter_mean,area_mean - 99%
radius_worst,perimeter_worst - 99%
radius_worst,area_worst - 98%
area_worst,perimeter_worst - 98%
dropped the columns perimeter_mean,area_mean,perimeter_worst,area_worst

visually showed the relation using scatterplot
left with 26 features after removal of correlated features

train_data : test_data = 0.8:0.2

Implemented SVM machine learning model with "rbf" and "linear" kernels and trained both models with train_data

Observed accuracy on test_data from both models are same, which is 95.6% 

svm1:
precision    recall  f1-score   support

           0       0.97      0.96      0.97        72
           1       0.93      0.95      0.94        42

    accuracy                           0.96       114
   macro avg       0.95      0.96      0.95       114
weighted avg       0.96      0.96      0.96       114


svm2 : 
precision    recall  f1-score   support

           0       0.95      0.99      0.97        72
           1       0.97      0.90      0.94        42

    accuracy                           0.96       114
   macro avg       0.96      0.95      0.95       114
weighted avg       0.96      0.96      0.96       114

Selcting svm2 model with "linear" kernel is encouraging as it has less false positives compared to svm1 even thoough they are having same accuracy_score
Recall for 0 is higher in second model
