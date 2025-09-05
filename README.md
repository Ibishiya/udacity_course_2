Data Analysis Key Findings
The dataset contains 1,872,830 transactions with 11 features, including step, type, amount, account balances, and the target variable isFraud.
There is a severe class imbalance in the target variable isFraud, with only 1,882 fraudulent transactions compared to 1,870,947 non-fraudulent ones.
A small number of missing values (1) were found in several columns (nameDest, oldbalanceDest, newbalanceDest, isFraud, isFlaggedFraud).
The isFlaggedFraud column had only one unique value (0.0) and was not useful for discrimination.
The nameOrig and nameDest columns had very high cardinality.
After data preparation (handling missing values, dropping irrelevant columns, one-hot encoding 'type', and scaling numerical features), the data was split into training (1,310,980 rows) and testing (561,849 rows) sets, maintaining the class distribution through stratification.
A RandomForestClassifier with balanced class weights was trained to address the class imbalance.
The trained model achieved high overall accuracy (1.00).
For the fraudulent class (1.0), the model achieved a precision of 0.99 (correctly predicting fraud 99% of the time it predicted fraud) and a recall of 0.73 (identifying 73% of actual fraudulent transactions).
The confusion matrix showed 4 false positives (legitimate transactions flagged as fraud) and 151 false negatives (fraudulent transactions missed by the model) on the test set.
Insights or Next Steps
While the model shows high precision for fraud detection, the recall of 0.73 indicates that a significant number of fraudulent transactions are not being identified. Further investigation into optimizing the model or employing advanced data balancing techniques could improve the detection rate of actual fraud.
The high cardinality of nameOrig and nameDest was handled by dropping these columns. Exploring alternative approaches like feature hashing or embedding could potentially incorporate information from these columns into the model if deemed important.
