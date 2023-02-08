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

    'EIN' and 'NAME' — Identification columns
    'APPLICATION_TYPE' — Alphabet Soup application type
    'AFFILIATION' — Affiliated sector of industry
    'CLASSIFICATION' — Government organization classification
    'USE_CASE' — Use case for funding
    'ORGANIZATION' — Organization type
    'STATUS' — Active status
    'INCOME_AMT' — Income classification
    'SPECIAL_CONSIDERATIONS' — Special consideration for application
    'ASK_AMT' — Funding amount requested
    'IS_SUCCESSFUL' — Was the money used effectively

- Software:
- [Google Colaboratory](https://colab.research.google.com)
- [Visual Studio Code, 1.70.2](https://code.visualstudio.com/updates/v1_70)
- [Jupyter Notebook 6.4.8](https://jupyter-notebook.readthedocs.io/_/downloads/en/v6.4.8/pdf/)
- [Python 3.9.12](https://www.python.org/downloads/release/python-3912/)
  - [tensorflow](https://www.tensorflow.org)
  - [scikit-learn](https://scikit-learn.org/stable/)

## Results

### Data Preprocessing

- What variable(s) are considered the target(s) for your model?
  - The 'IS_SUCCESSFUL' column is our model's target. This column is the bianary classifier we will use to predict if applicants will be sucessful should Alphabet Soup fund them.
- What variable(s) are considered to be the features for your model?
  - 'APPLICATION_TYPE','AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT' are the features for our model.
  - We also removed two features - 'EIN' and 'NAME'
- What variable(s) are neither targets nor features, and should be removed from the input data?
  - 'APPLIC

### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
  - The model's target / predictioed outcome, IS_SUCCESSFUL 

- Were you able to achieve the target model performance?
- What steps did you take to try and increase model performance?

## Summary
