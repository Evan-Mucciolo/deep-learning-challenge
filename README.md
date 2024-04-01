# Overview

This machine learning model and analysis was carried out with for the nonprofit foundation Alphabet Soup, who wants a tool to help it select applicants for funding with the best success in their ventures.

A dataset with 34,000 organizations was used for analysis along with several metrics Alphabet Soup keeps on it's applicants. The goal was to use this data to find out whether or not an application will be successful.

# Results

* Data Preprocessing
    * The target variable for our model was IS_SUCCESSFUL, which is a binary yes/no indicator on if the applicant was successful in their venture.
    * The features for our model included application type, affiliation, classification, use case, organization type, status, income amount, special consideration, and ask amount (how much money the applicant asks for).
    * The variables that were removed from the data that were not targets nor features were EIN and the organization Name.

* Compiling, Training, and Evaluating the Model
    * The model started with 80 neurons in the first hidden layer and decreased over the next layer to 30. There were 3 hidden layers used inlcuding the output layer and the relu activation function was used along with the sigmoid function in the final output layer. The number of neurons and layers were selected to increase the model capacity as there were 43 input dimensions. 
    * The target model performance of greater than 75% accuracy was not achieved during optimization. The closest outcome was 73%. 
    * Attempts to increase model peformance included changing the number of hidden layers from 2 to 3, increasing the number of epochs from 100 to 200, increasing the neurons in the second layer from 30 to 80, and changing the binning of the classification field to have more values. 

# Summary

Overall, the models settled around 73% accuracy regardless of the changes made in optimizing the model. This accuracy is greater than the number of successful marks in the original data, which was around 50%. This means it appears Alphabet Soup could get around 50% of applicants to be successful based on whatever method was used before. This was calcualted simply by taking the original CSV data and taking the number of successful applicants in the 'IS_SUCCESSFUL' column and dividing it by the total applicants. 

If our model can be accurate nearly three quarters of the time then Alphabet Soup will have their rate of successful applicants increase from where they currently stand. Because of this, I would recommend the model. 

Using a different model might yield an even better result. A linear regression model can also be used to predict a binary outcome, it may be better served to use principal component analysis to find what features matter most to a successful applicant venture and use that to create a model.  