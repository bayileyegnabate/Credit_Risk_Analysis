# Credit Risk Analysis
The purpose of this analysis is to evaluate credit risk using scikit-learn and imbalanced learning libraries. We will use different oversampling, undersampling techniques before applying Logistic Regression; employ Balanced Random Forest and Easy Ensemble classifiers.

## Results:
The main result are discussed bellow using the confusion matrix and the classification report tables.

### Naive Random Oversampling 

- the **confusion matrix** shows that out of the 101 high-risk credit card applications, we were able to flag only 71 of them. 

|                | predicted high risk | predicted low risk    |
|----------------|:---------------------:| :------------------:|
|actual high risk| 71                  | 30                |
|actual low risk | 7073                | 10031             |


- `balanced accuracy score ≈ 64%`


### SMOTE Oversampling

- using the SMOTE oversampling we predicted 64 of them as high rsik.  

|                | predicted high risk | predicted low risk    |
|----------------|:---------------------:| :------------------:|
|actual high risk| 64                  | 37                |
|actual low risk | 5286                | 11818             |


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

 |   |pre  |rec  |spe  |f1   |geo  |iba  |sup |
 |---|:---:|:---:|:---:|:---:|:---:|:---:|:---|
 |high_risk|0.01 | 0.81 | 0.56| 0.02| 0.67| 0.46| 101|
 |low risk |1.00 | 0.56| 0.81 | 0.71| 0.67| 0.44| 17104|
 |avg/total|0.99 | 0.56| 0.81 | 0.71| 0.67 | 0.44 | 17205|
 
 
 In conclusion, the SMOTEENN algorithm gives the highest best score in capturing the high-risk application. 