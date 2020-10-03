# Network-Intrusion-Detection

## Problem Statement
Software to detect network intrusions protects a computer network from unauthorized users, including perhaps insiders. This project aims to build a network intrusion detector, a predictive model capable of distinguishing between bad connections, called intrusions or attacks, and good normal connections.Model this problem as a BINARY classification problem. Use the following models to detect bad connections (intrusions).

## Methodology:
- Data pre-processing in which contains import the dataset, finding out the missing values, encoding the categories data, finding correlated features, splitting       the dataset.
- Feature normalization using Z-score.
- Applied Logistic Regression, Nearest Neighbor, Support Vector Machine and Fully-Connected Neural Networks with multiple combination of Activation function and Optimizer.
- Applying the models and generating classification report, Confusion matrix and ROC curve to compare the performance of models.
- Parameter tuning to compare model with different parameters.
    
## Comparsion of all models accuracy



## Challenges
### Balancing the data to improve the accuracy
While performing one-hot encoding on the categorical features, I found that the train set and test set had inconsistency in the number of features. For instance, in the below image we can see that the feature state has inconsistent values in train and test. So, I selected the first 4 occurrence of values in state and removed other values to avoid inconsistency.

### Detecting the best feature for target variable
Before I performed correlation analysis, I selected all the features for training Logistic Regression, and I obtained the precision and recall score 100%. This imposed that the model has been overfitting. So, I performed correlation analysis on the categorical and discrete features and removed highly correlating features. This time we increased the limit value to 0.9

### Parameter tuning to find the best neural network model
I performed multiple neural network model by tuning the parameter i.e. Activation function and Optimizer.

## Multi-Class Classification
### Detected the network intrusion for multi-class classification problem
For multi-class classification I removed the label feature and set the new target variable as attack_cat which contains the type of network intrusion. I used the same Activation function and Optimizer for neural network model which perform the best for binary classification. Accuracy achieved in multi-class classification is 86%.
