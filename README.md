# Module_12_Challenge
Supervised Learning. 



## Overview of the Analysis 

  The purpose of this analysis was to find out which model performed better at predicting creditworthiness of borrowers. 

* The historical data contained the following information:
  
  > ['loan_size,	interest_rate,	borrower_income,	debt_to_income,	num_of_accounts,	derogatory_marks,	total_debt']. 

- The y value was set to "loan_status", and the remaining columns were used as the features.

- We used a logistic regression model to compare two versions of the dataset.
  - First we used the original data.
  - Then we resampled the data by using the `RandomOverSampler` module from the imbalanced-learn library, and made predictions on the resampled data.
  

- We tried to preditct the "loan_status" as a 0 or 1.

    
   * A value of 0 in the “loan_status” column means that the loan is healthy.

   * A value of 1 means that the loan has a high risk of defaulting.
  

These are the steps we performed on both versions of the dataset:

>*  Get the of the count the target classes.
> * Train a logistic regression classifier.
> * Calculate the balanced accuracy score
> * Generate a confusion matrix.
> * Generate a classification report.


----

## Results


* Model 1: Logistic Regression Model with the Original Data:
  * Balanced Accuracy Score: 0.9520479254722232
  * Precision: 0.99
  * Recall: 0.99
```
                   pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.91      1.00      0.95      0.91     18765
          1       0.85      0.91      0.99      0.88      0.95      0.90       619

avg / total       0.99      0.99      0.91      0.99      0.95      0.91     19384
```

---
* Model 2: Logistic Regression Model with Resampled training Data. 
  * Balanced Accuracy Score: 0.9936781215845847
  * Precision: 0.99
  * Recall: 0.99
```
                   pre       rec       spe        f1       geo       iba       sup

          0       1.00      0.99      0.99      1.00      0.99      0.99     18765
          1       0.84      0.99      0.99      0.91      0.99      0.99       619

avg / total       0.99      0.99      0.99      0.99      0.99      0.99     19384

```


## Summary

* The model that performs the best would depend on your goal. 

* The model with original data does performs better at finding healthy loans.

* The model with resampled data performs better at prediciting high-risk loans, so I would reccomend this model for this specific use.


---


## Technologies
We need the imbalanced-learn and PyDotPlus libraries added to our dev virtual environment.

```
conda install -c conda-forge imbalanced-learn
conda install -c conda-forge pydotplus
```
---
## Usage

Our data is located in the "Resources" folder of this repo. 

---

## Contributors


G. Cale McDowell



[@gcm107](https://github.com/gcm107)

---

## License


