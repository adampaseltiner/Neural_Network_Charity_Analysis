# Neural_Network_Charity_Analysis

## Analysis Overview
The purpose of this project was to use deep-learning neural networks with the TensorFlow library in Python to help analyze and predict the risk of donation recipients from the Alphabet Soup nonprofit organization. 

## Results
### Data Preprocessing
- We began by cleaning the data and removing the `EIN`and `NAME` columns since they are identification information and add no value to the model
- The following columns `APPLICATION_TYPE` `AFFILIATION` `CLASSIFICATION` `USE_CASE` `ORGANIZATION` `STATUS` `INCOME_AMT` `SPECIAL_CONSIDERATIONS` `ASK_AMT` are the features for our model. The features have been split into training and testing datasets and standardized.
- The `IS_SUCCESSFUL` column contains binary data on whether a charity donation was used effectively and is thus considered the target for the deep learning neural network.

### Compiling, Training, and Evaluating the Model
Of my three attempts to reach the 75% performance target, below are the features of the model which came closest:
- 80 neurons (layer 1), 35 neurons (layer 2), 10 neurons (layer 3). All neurons (hidden layers) had a `ReLU` function and I used a `sigmoid` function for the output layer since it is best for a binary classification. For the compilation the optimizer is `adam` and the loss function is `binary_crossentropy`.
- The model accuracy only came in at 73% which is less than ideal for predicting the outcome of the charity donations.
- To try and make the model more accurate I added more hidden layers, and changed the number of neurons in each layer from previous attempts.

![Model1](https://user-images.githubusercontent.com/82347825/131736539-24c9a46e-ca49-4bb4-ab2b-0a3089dba313.png)
![Model2](https://user-images.githubusercontent.com/82347825/131736551-84d19b25-5d11-4292-a31b-fb185f4b7a5c.png)


## Summary
With the model accuracy only ending up around 73%, this was not the most effective analysis to predict the outcomes of the charity donations, although acheiving this high of an outcome was surprising giving the limited amount of data with which we were given to work and it is possible that with more data added to the model the accuracy would have been higher. It would also be prudent to consider using a random forsest model since it can randomly sample the preprocessed data and build smaller, simpler decision trees.
