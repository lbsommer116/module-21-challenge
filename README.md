# module-21-challenge

### See jupyter notebook files for original and optimized models

Overview of the analysis: Purpose of the analysis was to build a tool to help select applicants for funding who will have the best chance of success based on many historical factors that are used to measure success. Used features from the provided data to create classifier to predict whether applicatns will be successful if funded by the company.

Results: Using bulleted lists and images to support your answers, address the following questions:

Data Preprocessing

What variable(s) are the target(s) for your model? The target is whether the applicant was successful with the funding received.

What variable(s) are the features for your model? The features are all the other columns. 
*EIN and NAME—Identification columns
*APPLICATION_TYPE—Alphabet Soup application type
*AFFILIATION—Affiliated sector of industry
*CLASSIFICATION—Government organization classification
*USE_CASE—Use case for funding
*ORGANIZATION—Organization type
*STATUS—Active status
*INCOME_AMT—Income classification
*SPECIAL_CONSIDERATIONS—Special considerations for application
*ASK_AMT—Funding amount requested

What variable(s) should be removed from the input data because they are neither targets nor features?
In optimizing my model, I removed the "SPECIAL_CONSIDERATIONS" and "ORGANIZATION" columns that I didn't think were crucial for training the model.

Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?
In order to optimize my model, I used 5 layers and varied the numbers of neurons in each layer. I tried several activation functions, but relu seemed like the best one. I tried to use the keras tuner to tune the hyperparameters, but for some reason, it was freezing in the process, so I had to tune it myself. 

Were you able to achieve the target model performance?
I was not able to achieve optimal target model performance due to not being able to run the keras tuner, but I did get some optimization in my modek. 

What steps did you take in your attempts to increase model performance?
To increase model performance I did the following:
* Removed some columns from the dataset that seemed less important to train the model on
* Added layers to the model
* Increased the number of neurons within the model.
  
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
Overall, my accuracy was only around .73, however, if I were to be able to use the keras tuner, I think I couldn've gotten the accuracy to be much higher. I do also believe I could've used other ways to evaluate the model aside from accuracy, as accuracy may not be a great measure if the split between test and train isn't even. I could've used recall or precision to evaluate the model as well. At a higher accuracy, the model could help evaluate whether applicants will be successful depending on their features. 

