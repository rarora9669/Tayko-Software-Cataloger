# Tayko-Software-Cataloger (Data Mining using R programming)

1. Each catalog costs approximately $2 to mail (including printing, postage, and mailing costs). Estimate the gross profit that the firm could expect from the remaining 180,000 names if it selects them randomly from the pool. 

2. Develop a model for classifying a customer as a purchaser or nonpurchaser.
a. Partition the data randomly into a training set (800 records), validation set (700 records), and test set (500 records).
b. Run stepwise logistic regression using backward elimination to select the best subset of variables, then use this model to classify the data into purchasers and nonpurchasers. Use only the training set for running the model. (Logistic regression is used because it yields an estimated “probability of purchase,” which is required later in the analysis.) 

3. Develop a model for predicting spending among the purchasers. 
a. Create a vector of ID’s of only purchasers’ records (Purchase = 1).
b. Partition this dataset into the training and validation records. (Use the same training/validation labels from the earlier partitioning; one way is to use function intersect() to find IDs of purchasers in the original partitions). 
c. Develop models for predicting spending, using: 
i. Multiple linear regression (use stepwise regression)
ii. Regression trees 
d. Choose one model on the basis of its performance on the validation data.

4. Return to the original test data partition. Note that this test data partition includes both purchasers and nonpurchasers. Create a new data frame called Score Analysis that contains the test data portion of this dataset. 
a. Add a column to the data frame with the predicted scores from the logistic regression.
b. Add another column with the predicted spending amount from he prediction model chosen. 
c. Add a column for “adjusted probability of purchase” by multiplying “predicted probability of purchase” by 0.107. This is to adjust for over sampling the purchasers (see earlier description).
d. Add a column for expected spending: adjusted probability of purchase × predicted spending. 
e. Plot the lift chart of the expected spending. 
f. Using this lift curve, estimate the gross profit that would result from mailing to the 180,000 names on the basis of your data mining models. 


