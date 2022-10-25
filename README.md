# Neural_Network_Charity_Analysis
## Overview of the analysis
 - The purpose of this analysis is to use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
## Results
### Data Preprocessing
#### What variable(s) are considered the target(s) for your model?
 - Succesful
#### What variable(s) are considered to be the features for your model?
 - Application type, classification, usecase, organization, income amount, status, special considerations, and ask amount.
#### What variable(s) are neither targets nor features, and should be removed from the input data?
 - EIN and NAME
### Compiling, Training, and Evaluating the Model
#### How many neurons, layers, and activation functions did you select for your neural network model, and why?
 - Input features 42, first hidden layer 80, and second hidden layer of 30 and outer layer of 1. The hidden layer activation functions were relu and the outer layer is signoid. The sigmoid function is identified by a characteristic S curve. It transforms the output to a range between 0 and 1. The Rectified Linear Unit (ReLU) function returns a value from 0 to infinity, so any negative input through the activation function is 0. It is the most used activation function in neural networks due to its simplifying output, but it might not be appropriate for simpler models. In the second attempt, input features had the same 42 neurons, 80 first layer, 50 second, 5 and 5 for the third and fourth. I wanted to see if increasing the neurons would result in increased accuracy.
#### Were you able to achieve the target model performance?
 - The first attempt achieved a target performance of 0.646. In the second attempt, the target performance was increased to 0.728. No we were not able to achieve target of 75.
#### What steps did you take to try and increase model performance?
 - Adding third and fourth hidden layer.
 - Changing the binning of classification_counts to 1250 vs 1000. Also changing the binning of application_counts to 700 from 500.
 - Removing status and special considerations in the analysis but it resulted in a lower accuracy score.
 - Checked if there were any NaN within the dataset, but none were found.
 - Tried Adamax and Adagrad optimizers and both have resulted in a lower accuracy score compared to Adam.
## Summary
 - The purpose of this analysis is to use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
 - In the first attempt, we achieved an accuracy score of 0.646. To optimizie the accuracy score, I added a third and fourth hidden layer, changed the binning of application_counts to 700 from 500, I tried removing status and special considerations in the analysis but it resulted in a lower accuracy score, removing other columns but that also resulted in lower accuracy score, and I’ve also tried Adamax and Adagrad optimizers and both have resulted in a lower accuracy score compared to Adam.
 - The two biggest disadvantages to using a neural network model are that the layers of neurons are often too complex to dissect and understand, and neural networks are prone to overfitting.
 - Another solution to this problem is using a random forest classifier or a decision tree algorithm. 
