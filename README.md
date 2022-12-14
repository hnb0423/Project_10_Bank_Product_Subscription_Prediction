# Project_10_Bank_Subscription_Prediction

### Business Problem: 
Portuguese Banking Institution is looking to use marketing campaign data to assess if bank term deposit would be subscribed by client. 

### Goal: 
Predict if the client will subscribe to a bank term product.

### EDA
- Basic data insights <br/>
- Check multicollinearity among numeric variables<br/>
- Check distribution of numeric variables using boxplot<br/>

### Data Preprocessing
- Hanlde missing value using linear interpolation

### Feature Engineering
- Encode variables<br/>
- Change pdays variables from numeric to categorical<br/>
- Drop duration column<br/>


#### Resolve imbalanced trian data: oversample minority data using SMOTE technique
**Steps of smote:**
- Random sample from the minority class.
- Identify the k nearest neighbors.
- Take one of those neighbors and identify the vector between the current data point and the selected neighbor.
- Multiply the vector by a random number between 0 and 1.
- To obtain the synthetic data point, add this to the current data point

**So I used balanced train data to train model and predict on imbalanced test data**


#### Model Training & Evaluation
- Ensure balanced class weight
- Use RandomizedSearchCV to tune hyperparameters for each model
- Apply 5-fold cross validation
- Evaluate model using, f1 score, precision,and recall because test data is not balanced.I care more about whether the models can capture 1 instead of 0.
- Plot confusion matrix
- Plot precision & recall curve for all models
- Result summary table

#### Result
- Achieved 87% prediction accuracy and 61% recall score
