# Key factor prediction for candidature

### Model Architecture

![image](https://user-images.githubusercontent.com/60923910/132124801-ac9cf1ef-aa11-4dc3-902a-2c97775433f8.png)

### Model Workflow

![image](https://user-images.githubusercontent.com/60923910/132124824-a7e6f402-4ee2-4a55-a616-64c6848d2d63.png)

### Process done to achieve result

* Data analysis: To understand the data and to think about proper modelling.
* Feature engineering: Done feature engineering to give clear information to the model.
* Training and validation: Trained multiple models and validated the results to choose the best model.
* Hyper-parameter tuning:  Used Bayesian optimization to find the best hyper-parameter for the model.

### Pre-processing steps

* For Classifier:
  * Took all the columns except identifiers i.e. “Name” and “EmpID”.
  * Mapped the values of column “GraduatingInstitute” from {Tier 1, Tier 2, Tier 3} to {3,2,1} respectively. It provides ordinal information to the model.
  * Replaced “ExpectedCTC” with “ExpectedHike”.
  * Done One hot encoding using pandas’ “get_dummies” function.
 
* For Regressor:
  * Took all the columns except identifiers i.e. “Name” and “EmpID”.
  * Mapped the values of column “GraduatingInstitute” from {Tier 1, Tier 2, Tier 3} to {3,2,1} respectively. It provides ordinal information to the model.
  * Replaced “ExpectedCTC” with “ExpectedHike”.
  * Added column “BiasInfluentialFactor” predicted from classifier to the input data.
  * Done One hot encoding using pandas’ “get_dummies” function.

##### -----------------EOS-------------------------------
