## Overview of the Analysis

The goal of this machine learning analysis was to create a binary classifer that is capable of predicting whether applicants will be successful if funded by a charity. This involved taking a deep dive into neural networks.

### Data Preprocessing
1. What variable(s) are considered the target for your model?
---> The target for the model is the "Is-Successful" column.

2. What variable(s) are considered to be the features for your model?

---> NAME, APPLICATION, TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT,SPECIAL_CONSIDERATIONS, STATUS, and ASK_AMT

3. What variable(s) are neither and should be removed from the input data? 

---> EIN (Employer identificaiton) was dropped because the numbers could confuse the system into thinking its significant.

---> A student could drop SPECIAL_CONSIDERATIONS because there is only a small percentage of cases that had any special consideration, and special considerations cannot be quantified.

---> A student could drop STATUS because  all rows were the same value, 1.

### Compiling, Training, and Evaluating the Model

1. How many neurons, layers, and and activation functions did you select for your neural network model, and why?

---> In this model there are three hidden layers each with many neurons,  because this seeemed to increased the accuracy above 72%. The number of epochs wasn't changed. The first activation function was 'relu' but the 2nd and 3rd were 'sigmoid'and the output function was 'sigmoid'. Changing the 2nd and 3rd activation functions to 'sigmoid' also helped boost the accuracy.

2. Were you able to achieve the target model performance?
---> Yes 

3. What steps did you take to try and increase model performance?

---> It required converting the NAME column into data points, which has the biggest impact on improving efficiency. And, it also required adding a third layer and using the "sigmoid" activation function for the 2nd and 3rd layer.

## Summary

Overall, by increasing the accuracy above 75% we are able to correctly classify each of the points in the test data 72% of the time. And, an applicant has a 80% chance of being successful if they have the following:
* The NAME of the applicant appears more than 5 times (they have applied more than 5 times)
* The Type of APPLICATION is one of the following; T3, T4, T5, T6, T7, T8, T10, and T19
* The application has the following CLASSIFICATION; C1000, C2000, C3000, C1200, and C2100.

Random Forest is good for classification problems. Using this model produces a 77% accuracy.
