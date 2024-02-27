# Overview

The purpose of this analysis was to fit a model to the data of Alphabet Soup's funding for business ventures. The hope is to use this model to predict where their funding can be best utilized in the future, based on a variety of factors about the applicants.

# Results

* Data preprocessing
** The target variable for the model was whether or not the organization was successful (IS_SUCCESSFUL)
** The feature variables of the model were the application type, classification of the applicant, use case, income amount, ask amount, status, and whether or not there are special considerations for the applicant.
** The company Name and EIN are completely insignificant variables for this analysis, and were removed.
  
* Compiling, Training, and Evaluating the Model
** In the final model, I used a model with 5 layers, all of which utilize sigmoid activation, and the final layer utilizes sigmoid activation, as well.
** This model was chosen from a tuning process utilizing Hyperband tuning and selecting from a range of 1-10 layers, 20-150 neurons, and the relu, tanh, sigmoid, or softmax activation functions for the hidden layers.
** This model had an accuracy of 73%.
** I was not able to achieve the target performance, but I attempted to do so using Random Forest, to eliminate any potential insignificant features, model tuning, to improve value accuracy, and adjusting the bins for the Application Type and Classification variables.
*** Of these options, only tuning bore any fruit; the rest only lowered accuracy.

# Conclusion

In summary, the model achieved an accuracy of 73% through the use of Hyperband tuning. It did not achieve the overall goal of >75%, but it is fairly close. A decision tree might prove a useful alternative model for this dataset, as the data is almost entirely categorical, and the output is binary (success or failure)
