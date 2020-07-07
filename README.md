# Detroit Blight Violation Prediction [WIP]
The final assignment on Coursera Applied Machine Learning Course by University of Michigan. The objective is to predict whether or not blight violator comply to its fine given the data. **This project core goal is for the author to learn more about applied machine learning techniques and to familiarize with the field**

## PART 1 - Introduction to The Project and Model Selection

### INTRODUCTION

In this project, we will create a predictive model to see whether blight violators in Detroit will comply and pay the fine or not.<br>
In the training data, if the ticket was paid early, on time, or within one month of the hearing data the violators will be marked as **True** (1), if the ticket was paid after the hearing date or not at all the violators will be marked as **False** (0).
<br><br>
Several model/classifier and feature engineering will be performed in this project to be compared. The model that will be used are:
1. Gradient Boosted Tree
2. Random Forest
3. SVC
4. Naive Bayes Classifier

Several metrices will also be used as the model assessment, however, the Area Under the ROC Curve (AUC) will be our main metric. List of metrices will be used:
1. **Area under the ROC curve (AUC)**
2. Confussion Matrix
3. Precision, Recal, F1

### Conclusion on Part 1



Without performing any preprocessing and parameter tuning, we see that from the 'money' fields, **Gradient Boosted Tree Classifier** performs best compared to other classifier (Random Forest, Gaussian Naive Bayes, and SVC). This is based on their ROC score, detailed as follows:

1. GBC : 0.756
2. RF  : 0.755
3. GNB : 0.704
4. SVC : 0.637

GBC performs insignificantly better than RF, this is also consistent to their confussion matrix.<br>
In this type of data, SVC perform the worst also in its runtime length. I also tried to rescale the data for the SVC, but the result is oddly even worse than the default SVC.
<br><br>
For the next part, we will dig more on feature engineering and parameter tuning to improve ROC score of the GBC
