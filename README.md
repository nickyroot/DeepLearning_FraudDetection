# DeepLearning_FraudDetection

*Author: Nick Root*

I have for some time been working on fraud detection problems and feel it is my duty to share the result of that work so it can be used more widely if at all useful.

# The data

The data set is available on Kaggle for download - https://www.kaggle.com/dalpozz/creditcardfraud

In summary, it contains 284,807 credit card transactions over 48 hours. It totally contains two types of transactons - fraud and genuine - inside the label column named 'Class'

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, no more information is provided regarding the original features and more background information about the data. Features V1, V2, ... V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise."

AS with most fraud data, it is very imbalanced - around 0.17% are fraud and the rest are all genuine. The challenge is to build a decent model that is able to tell which are fraud transactions based on the given features of around 30 in total. Area Under the ROC Curve (AUC) score is recommended as model evaluation criterion given the unbalanced nature of data. 

# Models used

These are models and techniques that I have developed in professional roles that I was keen to test on a public dataset

Both have achieved around 0.95 AUC score on val set, generalising to this data better than I expected. I used the exact same method, albeit with a lot more cleansing, on a much larger bank dataset and achieved around 0.93 AUC score.

There is a RBM as well as an Auto-encoder
