# Neural_Network_Charity_Analysis

Module 20: Neural Networks and Deep Learning Models

## Background

We've been tasked with utilizing our knowledge of Neural Networks and Machine learning to assist Alphabet Soup in predicting where to make investments. To do this, we'll use the features in the dataset to create a binary classifier capable of predicting whether applicants will be succesful if funded by the foundation.

## What We're Creating

This new assignment consists of three technical analysis deliverables and a written report:

- Deliverable 1: Preprocessing Data for a Neural Network Model
- Deliverable 2: Compile, Train, and Evaluate the Model
- Deliverable 3: Optimize the Model
- Deliverable 4: A Written Report on the Neural Network Model (README.md)

## Resources

- Data Source:
  - [charity_data.csv](https://github.com/abrodyyy/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv)
  - From Alphabet Soup’s business team, we've received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as the following:

   - `EIN` and `NAME` — Identification columns
   - `APPLICATION_TYPE` — Alphabet Soup application type
   - `AFFILIATION` — Affiliated sector of industry
   - `CLASSIFICATION` — Government organization classification
   - 'USE_CASE' — Use case for funding
   - `ORGANIZATION` — Organization type
   - `STATUS` — Active status
   - `INCOME_AMT` — Income classification
   - `SPECIAL_CONSIDERATIONS` — Special consideration for application
   - `ASK_AMT` — Funding amount requested
   - `IS_SUCCESSFUL` — Was the money used effectively

- Software:
- [Google Colaboratory](https://colab.research.google.com)
- [Visual Studio Code, 1.70.2](https://code.visualstudio.com/updates/v1_70)
- [Jupyter Notebook 6.4.8](https://jupyter-notebook.readthedocs.io/_/downloads/en/v6.4.8/pdf/)
- [Python 3.9.12](https://www.python.org/downloads/release/python-3912/)
  - [tensorflow](https://www.tensorflow.org)
  - [scikit-learn](https://scikit-learn.org/stable/)

## Results

### Data Preprocessing

1. What variable(s) are considered the target(s) for your model?
  - The `IS_SUCCESSFUL` column is our model's target. This column is the bianary classifier we will use to predict if applicants will be sucessful should Alphabet Soup fund them.
2. What variable(s) are considered to be the features for your model?
  - `APPLICATION_TYPE`,`AFFILIATION`, `CLASSIFICATION`, `USE_CASE`, `ORGANIZATION`, `STATUS`, `INCOME_AMT`, `SPECIAL_CONSIDERATIONS`, and `ASK_AMT` are the features for our model.
3. What variable(s) are neither targets nor features, and should be removed from the input data?
  - `EIN` and `NAME` are not targets or features and were removed from the input data. 

### Compiling, Training, and Evaluating the Model

1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
#### Original Model: 73.01 % accuracy
- Dropped `EIN` and `NAME`
- Binned `APPLICATION_TYPE` and replaced value counts < 500  
- Binned `CLASSIFICATION` and replaced value counts < 1000  
- hidden_nodes_layer1 --> 80 neurons with relu activation
- hidden_nodes_layer2 --> 30 neurons with relu activation
- output layer --> sigmoid activation
- 100 epochs to train the model 

2. Were you able to achieve the target model performance?
From the original model, we were only not able to reach an accuracy rate of 75% (target performance). We did take several steps to further optimize the model, however we were unable to reach the target. 

3. What steps did you take to try and increase model performance?

#### Optimization Attempt # 1 --> 72.87 % accuracy
Additional neurons are added to hidden layers
- Dropped `EIN` and `NAME`
- Binned `APPLICATION_TYPE` and replaced value counts < 1000  
- Binned `CLASSIFICATION` and replaced value counts < 1000 
- hidden_nodes_layer1 --> 160 neurons with relu activation
- hidden_nodes_layer2 --> 80 neurons with relu activation
- output layer --> sigmoid activation
- 100 epochs to train the model 

#### Optimization Attempt # 2 --> 72.87 % accuracy
Additional hidden layers are added
- Dropped `EIN` and `NAME`
- Binned `APPLICATION_TYPE` and replaced value counts < 1000  
- Binned `CLASSIFICATION` and replaced value counts < 1000 
- hidden_nodes_layer1 --> 160 neurons with relu activation
- hidden_nodes_layer2 --> 80 neurons with relu activation
- hidden_nodes_layer3 --> 40 neurons with relu activation
- output layer --> sigmoid activation
- 100 epochs to train the model 

#### Optimization Attempt # 3 --> 72.97 % accuracy
The activation function of hidden layers changed for optimization
- Dropped `EIN` and `NAME`
- Binned `APPLICATION_TYPE` and replaced value counts < 1000  
- Binned `CLASSIFICATION` and replaced value counts < 1000 
- hidden_nodes_layer1 --> 80 neurons with tanh activation
- hidden_nodes_layer2 --> 30 neurons with tanh activation
- output layer --> sigmoid activation
- 100 epochs to train the model 

#### Optimization Attempt # 4 --> 72.92 % accuracy
Increasing the number of epochs to the training regimen.
- Dropped `EIN` and `NAME`
- Binned `APPLICATION_TYPE` and replaced value counts < 1000  
- Binned `CLASSIFICATION` and replaced value counts < 1000 
- hidden_nodes_layer1 --> 80 neurons with relu activation
- hidden_nodes_layer2 --> 30 neurons with relu activation
- output layer --> sigmoid activation
- 200 epochs to train the model 

#### Optimization Attempt # 5 --> 73.03 % accuracy
Reducing the number of epochs to the training regimen.
- Dropped `EIN` and `NAME`
- Binned `APPLICATION_TYPE` and replaced value counts < 1000  
- Binned `CLASSIFICATION` and replaced value counts < 1000 
- hidden_nodes_layer1 --> 80 neurons with relu activation
- hidden_nodes_layer2 --> 30 neurons with relu activation
- output layer --> sigmoid activation
- 50 epochs to train the model 

#### Optimization Attempt # 6 --> 73.22 % accuracy
Using KerasTuner to find the best model 
- Dropped `EIN` and `NAME`
- Binned `APPLICATION_TYPE` and replaced value counts < 1000  
- Binned `CLASSIFICATION` and replaced value counts < 1000 

![KerasTuner](https://user-images.githubusercontent.com/111623064/217542842-50fabb04-2c89-4bfb-abf4-d1cecdcbadcf.svg)


## Summary
Unfortunatley, we were not able to reach the target accuracy rate of 75%, despite several optimization attempts. The model that got the closes was #6, where we used KerasTuner to try to determine the best model. I would reccomend further optimization attempts using KerasTuner, and we can likely reach our target. Another option would be look into other types of supervised machine learning in combination with an algorithm like  LightBGM or XGBoost. 
