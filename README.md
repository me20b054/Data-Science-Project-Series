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


Documentation for Stock Market Prediction:

Given dataset consists of 251 days of the year 2022 with 31 records in each day. (31x251 = 7781) 
All the prices "low","high","open","close" followed the same trend and selected "Closing price" is value to be predicted
lablencoded the category column "ticker" 
"date" column has been divided to day,month,year and dropped the year column as it is common for the whole dataset
Now the final features are
open	high	low	close	adjclose	volume	ticker    month    day

Scaled all the numerical features
split in the ratio 0.7:0.3 (train_data:test_data)

Utlised the regression models including linearRegression, RandomForestRegressor, GradientBoostRegressor with the followign MSE results on test_data

LinearRegression  - 0.4194253647496177
RandomForestRegressor - 1.6607168996246393
GradientBoostRegressor -1.4227079382621097
