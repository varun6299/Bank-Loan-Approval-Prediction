# Bank-Loan-Approval-Prediction
An Analytics Vidhya Hackathon

This is a Machine Learning Classification task as a part of the Loan Prediction Hackathon organized by Analytics Vidhya. The problem statements involves identifying which customers' loan requests would be rejected or approved.

Metric to increase was **ACCURACY**

Click here to view loan prediction competition - https://datahack.analyticsvidhya.com/contest/all/
**(THE COMPETITION MIGHT GET REMOVED AFTER DURATION FOR COMPETITION EXPIRES)**

### DATA CLEANING - 
- Datatype of certain columns were wrongly identified. Corrected them. 
- Categories names in certain feature not making sense. Categories names made clear. 

### EXPLORATORY DATA ANALYSIS - 
- Skewness and outliers detected in numerical features.
- Missing values detected in categorical and numerical features.
- No imbalance reported.
- Numerical features not useful in classifying records.
- Few categorical features showing patterns in differentiating approved and rejected loan requests.
- No multicollinearity.

### PREPROCESSING THE DATA - 
#### MISSING VALUE IMPUTATION - 
- Data split into train and test to avoid data leakage.
- To impute numerical features, used the simple imputer.
- To impute categorical features, used the weight of evidence method. Also encoding performed by woe.

#### OUTLIER TREATMENT - 
- Outliers couldnt be dropped due to high proportion and couldnt be capped due to large outliers.
- Numerical features were transformed.

### MODEL BUILDING - 
#### CREATING BASELINE MODELS -
- Logistic regression, KNN, SVC, Decision tree, Random Forest Model, Adaboost, Gradient Boosting and XGB Classifiers were used.
- Decision tree and ensemble techniques gave accuracy greater than 70%. Used for further improvement

#### PARAMETER TUNING - 
- Best parameters were found for each model using Grid Search.
- Accuracy scores touching 78% to 81%.
- Highest accuracy calculated for tuned decision tree on test i.e 81%.

#### STACKING TECHNIQUES - 
- Models were clubbed together to create super models using voting and stacking classifier.
- No improvement in performance.
- Best overall score on test - 80%

#### FEATURE SELECTION - 
- Best features found for stacked classifier using Forward Feature Elimination
- No improvement in accuracy.

### FINAL MODEL - 
- Stacked classifier with Tuned Decision Tree, Random Forest, Gradient, XGB and Adaboost classifier.

### SCORE ACHIEVED ON UNSEEN TEST / COMPETIION - 0.77 or 77% 
