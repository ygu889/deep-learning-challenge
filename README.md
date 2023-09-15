# deep-learning-challenge

## Overview of the Analysis

The purpose of this analysis is to build a deep learning model to predict whether organizations funded by Alphabet Soup will be successful in their ventures. The analysis involves preprocessing the dataset, designing a neural network model, training the model, and optimizing it to achieve a target predictive accuracy of higher than 75%. The target variable for our model is `IS_SUCCESSFUL`, which indicates whether the funding provided by Alphabet Soup was used effectively (binary classification - 1 for successful, 0 for unsuccessful).

## Results

### Data Preprocessing

- The target variable for our model is `IS_SUCCESSFUL`, which indicates whether the funding provided by Alphabet Soup was used effectively (binary classification - 1 for successful, 0 for unsuccessful).

- The feature variables for our model include all columns in the dataset except `EIN`. These features provide information about each organization, such as name, application type, affiliation, classification, use case, income amount, special considerations, and funding amount requested.

- Based on the attempts 1 and 2 I tried by removing more columns, however that did not appear to increase the accuracy of the model. So in the third attemp, I only removed the `EIN` (Employer Identification Number) columns as its is an identification column and not relevant for modeling.

- We used pd.get_dummies() to encode categorical variables, converting them into numerical format suitable for the neural network model.

### Compiling, Training, and Evaluating the Model

 I chose 4 hidden layers to capture complex patterns in the data. I also choose the neuros 120, 100, 80 and 50 for each of the layers and I tried the sigmoid activiation. The sigmoid function squashes its input into a range between 0 and 1. It is often used for binary classification problems because it naturally outputs probabilities. The sigmoid activation is more suitable than relu and tanh activation since for the model we use the features in the provided dataset to create a binary classifier. As indicated by the result of attempt 3, the accuracy went from 72% to 75%. 

 I was able to achieve the traget model performace on attempt 3 by dropping few columns only the EIN column, creting one more binning with the Ask_AMT and using 4 hidden layers, the sigmoid activiation, and reducing the number of epochos. 


### Summary

 After several attempts of optimization, I achieved a predictive accuracy of over 75%, meeting the target performance. The model showed its ability to effectively classify organizations as either successful or unsuccessful based on the provided features.

While the current model meets the target performance, there are additional improvements that can be explored:
- Further tuning: Continue fine-tuning hyperparameters to see if a higher accuracy can be achieved.
- Feature engineering: Experiment with feature selection or engineering to enhance the model's predictive power.
- More data: If available, collecting more data can help the model generalize better and potentially improve accuracy.
