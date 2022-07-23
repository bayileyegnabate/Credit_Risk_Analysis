# Credit Risk Analysis
The purpose of this analysis is to evaluate credit risk using scikit-learn and imbalanced learning libraries. We will use different oversampling, undersampling techniques before applying Logistic Regression; employ Balanced Random Forest and Easy Ensemble classifiers.

## Results:
The main result are discussed bellow using the confusion matrix and the classification report tables.

### Naive Random Oversampling 

- the **confusion matrix** shows that out of the 101 high-risk credit card applications, we were able to flag only 71 of them. 


|                | predicted high risk | predicted low risk  |
|----------------|:---------------------:| :----------------:|
|actual high risk| 71                    | 30                |
|actual low risk | 7073                  | 10031             |


- `balanced accuracy score ≈ 64%`


### SMOTE Oversampling

- using the SMOTE oversampling we predicted 64 of them as high rsik.  


|                | predicted high risk | predicted low risk  |
|----------------|:---------------------:| :----------------:|
|actual high risk| 64                    | 37                |
|actual low risk | 5286                  | 11818             |


- `balanced accuracy score ≈ 66%`


### Cluster Centroid Undersampling

- the CC undersampling gives a similar result as the naive random sampling interms of flagging the high risk applications. But it has a low accuracy score.  

|                | predicted high risk | predicted low risk  |
|----------------|:---------------------:| :----------------:|
|actual high risk| 70                    | 31                |
|actual low risk | 10324                 | 6780              |


- `balanced accuracy score ≈ 54%`



### Balanced Random Forest Classifier

- the Cluster Centroid undersampling gives a similar result as the naive random sampling interms of flagging the high risk applications. But it has a low accuracy score.  

|                | predicted high risk   | predicted low risk  |
|----------------|:---------------------:| :------------------:|
|actual high risk| 70                    | 31                  |              
|actual low risk | 10324                | 6780                 |


- `balanced accuracy score ≈ 54%`


### SMOTEENN (over and under) sampling
- a combination of over- and under-sampling results, as show in the confusion matrix bellow, was able to predic *82* of the 101 applications as *high risk*:

|                | predicted high risk   | predicted low risk  |
|----------------|:---------------------:| :------------------:|
|actual high risk| 82                    | 19                  |
|actual low risk | 7593 	             | 9511                |

- `balanced accuracy score ≈ 68%`


- imbalanced classification report:

 |         |pre  |rec  |spe  |f1   |geo  |iba   |sup  |
 |---      |:---:|:---:|:---:|:---:|:---:|:---: |:---:|
 |high_risk|0.01 |0.81 |0.56 | 0.02| 0.67 | 0.46|101  |
 |low risk |1.00 |0.56 |0.81 | 0.71| 0.67 | 0.44|17104|
 |avg/total|0.99 |0.56 |0.81 | 0.71| 0.67 | 0.44|17205|
 
 
 ### Easy Ensemble AdaBoost Classifier
 using the *Easy Ensemble Classifier* gives the best `balanced accuracy test` of `93%` Also, as shown in the confusion matrix, `EasyEnsembleClassifier`identifies 93 0f the 101 high-risk correctly. 
 
|                | predicted high risk   | predicted low risk  |
|----------------|:---------------------:| :------------------:|
|actual high risk| 93                    | 8                   |
|actual low risk | 983 	                 | 16121               |


- imbalanced classification report:

 |         |pre  |rec  |spe  |f1   |geo  |iba   |sup  |
 |---      |:---:|:---:|:---:|:---:|:---:|:---: |:---:|
 |high_risk|0.09 |0.92 |0.94 | 0.16| 0.93 | 0.87|101  |
 |low risk |1.00 |0.94 |0.92 | 0.97| 0.93 | 0.87|17104|
 |avg/total|0.99 |0.94 |0.92 | 0.97| 0.93 | 0.87|17205|
 
 In conclusion, the `EasyEnsembleClassifier` algorithm gives the highest best score in capturing the high-risk applications. 