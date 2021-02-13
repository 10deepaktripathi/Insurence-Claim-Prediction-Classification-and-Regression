company wants a modal that is not only predicting if an insured will claim but also the amount if s/he chose to claim. For this task too, we have historical data available, but this time target claim_amount is real valued feature. Target denotes the claimed amount by insured in the past and it is equal to 0 if an insured has not claimed. I have built 2 models for this task. One for classification and another for regression. Classification modal will classify if an insured claim or not. Regression modal will predict how much will s/he claim. Note that regression will work only if the result of classification is True.
For classification task I have created a new target feature whose value is False if claim amount (Target) in the CE802_P3_Data.csv file is 0, otherwise True. The new target we got by this procedure was making dataset highly imbalanced. So, to check the performance of classification modal I have used f1-score.
Also, I have removed the claim amount target feature for classification task after creating the new target.
In regression, below is a small summary of steps which i followed-

Feature Selection, 
One hot encoding, 
Ordinal Encoding, 
Scaling, 
Hyperparameter tunning, 
Training MLP.

Eventually I have used MLP with logistic regression to predict the test set provided by the company.
