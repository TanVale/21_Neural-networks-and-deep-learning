# 21_Neural-networks-and-deep-learning

# Overview of the analysis
The goal of this exercise is to attempt to create a model that can predict whether or not a venture will succeed. The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. A CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years was provided. Within this dataset are a number of columns that capture metadata about each organization, such as:
EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

# Results
![accuracy image]()
#Data Preprocessing
What variable(s) were the target(s) for the model? - The target variable is named "IS_SUCCESSFUL".
What variable(s) were the features for the model? - The features were derived from all other columns; I removed columns that were not useful for the model. I then used the "get_dummies()" method to expand some columns.
What variable(s) should be removed from the input data because they are neither targets nor features? - The four columns removed were: "EIN","NAME","STATUS","SPECIAL_CONSIDERATIONS" 

# Compiling, Training, and Evaluating the Model
Were you able to achieve the target model performance? - I was able to get the nodel to a 0.79 accuracy but adding three hidden layers. Initially I had only 3 layers with activation relu, softmax and sigmoid. To improve accuracy I added another layer and changed the activations. The first layer was still relu but I changed the next 3 layer's activations to sigmoid.

What steps did you take in your attempts to increase model performance? - I binned the "Name" column and used "Sigmoid" as the activation for the second, third and fourth layer. I also unbinned "income_amt" to improve accuracy. 

Summary: I was able to achieve an accuracy of 79% by adding another layer, changing the activation and binning/ unbinning some columns as well as dropping columns that did not help the model.
