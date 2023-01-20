# Neural_Network_Charity_Analysis
**Using neural networks to help a charity foundation predict where to make investments**

## Project Overview
A neural network is a powerful machine learning technique that is modeled after neurons in the brain. Neural Networks can rival the performance |of the most robust statistical algorithms without having to worry about any statistical theory. Industry leaders such as Google, Facebook, Twitter, and amazon use an advanced form of neural networks called Deep Neural Networks to analyze images and natural language processing datasets.

Using knowledge gained over machine learning models and neural networks, the features in this dataset will be used to create a binary classifer that will tell the customer whether or not potenial applicants will be successful funded by Alphabet Soup. The dataset contains more than 34,000 organizations that have received funding from Alphabet Soup.

This project will consist of three steps:
+ Preprocessing Data for the Neural Network Model
+ Compile, Train, and Evaluate the Model
+ Optimize the Model

## Results

### Data Preprocessing

+ What variable(s) are considered the target(s) for your model?
  The variable considered as focus or target for the model is the "IS_SUCCESSFUL" column.

+ What variable(s) are considered to be the features for your model?
  The features of the deep learning model are:
    + APPLICATION_TYPE
    + AFFILIATION
    + CLASSIFICATION
    + USE_CASE
    + ORGANIZATION
    + STATUS
    + INCOME_AMT
    + ASK_AMT

+ What variable(s) are neither targets nor features, and should be removed from the input data?
    + EIN
    + NAME
    + SPECIAL_CONSIDERATIONS

### Compiling, Training, and Evaluating the Model

+ How many neurons, layers, and activation functions did you select for your neural network model, and why?
    The model was made with input features and two hidden layers. The first hidden layer has 80 neurons, the second layer has 30 nuerons, and lastly there is an outer layer. There are three activation funcations, one per layer. The 1st and 2nd hidden layers have an activation function of "relu" while the outer layer's activation function is "sigmoid".

    In the first optimization, we tried to add the fourth layer, changing the neurons and keeping 50 epochs and not changing the activation function of hidden layers or output layers.

    In the second optimization, we removed one layer, changing the neurons again around half values compared to the first optimization, keeping 40 epochs. Also, we changed the activation function of hidden layers to 'tanh.'

    In the last optimization attempt, we returned similar parameters to the first optimization because we got a better result of accuracy (73.05) than the second optimization (72.97). So, we decided to change the neurons a bit, keeping the values close to the first optimizations; however, in this attempt, we decided to change the activation function of output layers to 'tanh' and the optimizer to 'Nadam". We got the best accuracy result compared with the three optimizations with 73.20.

+  Were you able to achieve the target model performance?
    No. The best result was 73.20%

+  What steps did you take to try and increase model performance?

+ First Optimization
    + Added two additional layers totalizing four.
    + hidden nodes layer 1 = 250
    + hidden nodes layer 2 = 140
    + hidden nodes layer 3 = 50
    + hidden nodes layer 4 = 20
    + We kept activation function of hidden layers as relu
    + We kept the activation function of output layers as sigmoid.
    + We kept the optimizer as adam
    + We changed the number of epochs to 50

+ Second Optimzation
    + Excluded one layer, totalizing three.
    + hidden nodes layer 1 = 100
    + hidden nodes layer 2 = 75
    + hidden nodes layer 3 = 50
    + We changed the activation function of hidden layers to tanh
    + We kept the activation function of output layers as sigmoid.
    + We kept the optimizer as adam
    + We changed the number of epochs to 40

+ Third Optimzation
    + Added one extra layer again, totalizing four.
    + hidden nodes layer 1 = 250
    + hidden nodes layer 2 = 120
    + hidden nodes layer 3 = 35
    + hidden nodes layer 4 = 15
    + We changed the activation function of hidden layers to relu
    + We changed the activation function of output layers as tanh.
    + We changed the optimizer as Nadam
    + We increased the number of epochs to 40


## Summary

The neural networks are not a definitive answer for all information data science issues as there are trade-offs to utilizing the new and famous neural network (and deep learning) models over their more established, frequently more lightweight statistics and machine learning counterparts.

For future analysis, we recommend other different models such as Random Forest, boosting and SVMs in order to increase the result accuracy.