
# Overview
The nonprofit foundation Alphabet Soup has funded many organizations. The csv file, https://static.bc-edx.com/data/dl-1-2/m21/lms/starter/charity_data.csv, contains data from over 34,000 organizations that have recieved funding from Alphabet Soup. The file, deep_learning_model_builder.ipynb, creates a deep learning model to create an algorithm to find which organizations are successful after recieving funding based on a number of criteria.

# Results

### Data Preprocessing
The model targets the 'IS_SUCCESSFUL' variable as this is what the model aims to predict. This varible identifies if the money received by Alphabet Soup's funding was used effectively. The following varibles are used to create this model: /

APPLICATION_TYPE—Alphabet Soup application type\
AFFILIATION—Affiliated sector of industry\
CLASSIFICATION—Government organization classification\
USE_CASE—Use case for funding\
ORGANIZATION—Organization type\
STATUS—Active status\
INCOME_AMT—Income classification\
SPECIAL_CONSIDERATIONS—Special considerations for application\
ASK_AMT—Funding amount requested\

The variables 'EIN' and 'NAME' are just used to uniquely identify each organization in the database, and are not important to the success of the funding. Therefore, are left out of the model. 

### Compiling, Training, and Evaluating the Model 
The neural_network() function was created first to quickly change the parameters of the model to optomize the model by hand. However, after trying a number of different models, the best model found had an accuracy of only 53.24%, which is not nearly as accurate as intended. The keras tuner was then used to automatically optimize the model much quicker than by hand. The best model that keras tuner found had an accuracy of 72.69%, which is much better than any model found by hand using the first method. The best model had 5 layers and used the sigmoid activation function. 

#  Summary
The best model achieved an accuracy of 72.69% and a loss of 58.28%. These results could possible be improved if more time is spent optimizing the model. The nerual_network function could be altered to fit more closely with the tuner's best model to get a somewhat better model. 

