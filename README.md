# deep-learning-challenge

# Report

## Overview
- The goal of this project was to create a neural network model that could predict the success of an application for funding.

## Results
Data Preprocessing:
- Target variables
    * IS_SUCCESSFUL
- Feature variables
    * APPLICATION_TYPE
    * AFFILIATION
    * CLASSIFICATION
    * USE_CASE
    * ORGANIZATION
    * STATUS
    * INCOME_AMT
    * SPECIAL_CONSIDERATIONS
    * ASK_AMT
- Removed variables
    * EIN
    * NAME

Compiling, Training, and Evaluating the Model
- For the initial model
    * 2 hidden layers with relu activation and 6 neurons.
    * Output layer of 1 neuron with sigmoid activation
    * Trained over 100 epochs
    * This number of hidden layers and neurons allowed a balance of computational power and resource usage.
    * Relu activation was a good starting point, because there was not a lot of negative values.
    * Sigmoid activation was used for the output due to it being able output a probability between 0 and 1.
    * Training on 100 epochs allowed a reasonable amount of tuning for the time needed to train.
- Model performance
    * Inital model tested at 72.24% accuracy.
    * Optimization attempts never increased accuracy over 73% when tested.
- Optimiation attempted by:
    * Removing the status variable
    * Creating an additional bin in classification
    * Having up to 4 hidden layers
    * Having up to 25 neurons in hidden layers
    * Changing various hidden layer activation functions to tanh or leaky relu
    * Changing the number of epochs between 20, 100, and 1000.

## Summary
The highest accuracy obtained was still less than 73%. This is too unreliable to use as a model. I would recommend trying a logistic regression model next. This model works best for a binary output like success and failure of applications, and the model would work with our scaled data.