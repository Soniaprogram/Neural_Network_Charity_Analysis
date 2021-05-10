# Neural_Network_Charity_Analysis


## Overview of the analysis:
For the non-profit organization Alphabet Soup, I designed a deep learning neural network that will predict if an Alphabet Soup funded organization will be successful based on features provided in the given dataset.

### Deliverable 1: Preprocessing Data for a Neural Network Model
Using my knowledge of Pandas and the Scikit-Learn’s StandardScaler(), I preprocessed the given dataset in order to compile, train, and evaluate the neural network model that will be developed in Deliverable 2.

### Deliverable 2: Compile, Train, and Evaluate the Model
Using my knowledge of TensorFlow, I designed a neural network, or deep learning model, to create a binary classification model that can predict if an Alphabet Soup funded organization will be successful based on the features in the dataset. I was required to think about how many inputs there were before determining the number of neurons and layers in my model. I then compiled, trained, and evaluated my binary classification model to calculate the model’s loss and accuracy.

<b> Reference: AlphabetSoupCharity.ipynb and AlphabetSoupCharity.h5 </b>

![img1](https://github.com/Soniaprogram/Neural_Network_Charity_Analysis/blob/main/images/del2model.PNG)
![img2](https://github.com/Soniaprogram/Neural_Network_Charity_Analysis/blob/main/images/del2evaluate.PNG)


### Deliverable 3: Optimize the Model
Using my knowledge of TensorFlow, I optimized my model in order to achieve a target predictive accuracy higher than 75%. I achieved an accuracy that was not higher than 75%, but very close (72.6%) after three attempts.

<b> Reference: AlphabetSoupCharity_Optimzation.ipynb and AlphabetSoupCharity_Optimzation.h5 </b>

#### Attempt 1:
![img3](https://github.com/Soniaprogram/Neural_Network_Charity_Analysis/blob/main/images/del3att1.PNG)
![img4](https://github.com/Soniaprogram/Neural_Network_Charity_Analysis/blob/main/images/del3att1eval.PNG)

#### Attempt 2:
![img5](https://github.com/Soniaprogram/Neural_Network_Charity_Analysis/blob/main/images/del3att2.PNG)
![img6](https://github.com/Soniaprogram/Neural_Network_Charity_Analysis/blob/main/images/del3att2eval.PNG)

#### Attempt 3:
![img7](https://github.com/Soniaprogram/Neural_Network_Charity_Analysis/blob/main/images/del3att3.PNG)
![img8](https://github.com/Soniaprogram/Neural_Network_Charity_Analysis/blob/main/images/del3att3eval.PNG)

## Results:

#### Data Preprocessing

<b> What variable(s) are considered the target(s) for your model? </b>
* IS_SUCCESSFUL would be a target for my model since it identifies if a donation was used for a successful organization

<b> What variable(s) are considered to be the features for your model? </b>
The following variables were features for my model:
* APPLICATION_TYPE
* AFFILIATION
* CLASSIFICATION
* USE_CASE
* ORGANIZATION
* STATUS
* INCOME_AMT
* SPECIAL_CONSIDERATIONS
* ASK_AMT

<b> What variable(s) are neither targets nor features, and should be removed from the input data? </b>
The following variables were neither targets nor features and were dropped:
* EIN
* NAME

#### Compiling, Training, and Evaluating the Model

<b> How many neurons, layers, and activation functions did you select for your neural network model? </b>

Attempt 1: 
* Neurons: 80, 30, 20
* Layers: 3 Hidden Layers
* Activation Functions: relu (first hidden layer), sigmoid (second, third, and output layers)
* Accuracy: 72.58%

Attempt 2 (Increased Hidden Layer):
* Neurons: 100, 50, 20, 10
* Layers: 4 Hidden Layers
* Activation Functions: relu (first hidden layer), sigmoid (second, third, fourth, and output layers)
* Accuracy: 72.55%

Attempt 3 (Changed Activation Function):
* Neurons: 100, 50, 20, 10
* Layers: 4 Hidden Layers
* Activation Functions: tanh (hidden layers), sigmoid (output layer)
* Accuracy: 72.62%
 
<b> Were you able to achieve the target model performance? </b>
* I was unable to achieve 75%, however, reached 72.6% after Attempt 3.

<b> What steps did you take to try and increase model performance? </b>
* I started out with 3 hidden layers in Attempt 1. I tried increasing the number of hidden layers from 3 to 4 in Attempt 2. Lastly, in Attempt 3, I changed the activation function for my hidden layers from relu and sigmoid to tanh. 


## Summary: 
In summary, Attempt 3 with 4 hidden layers and a tanh activation function for the 4 hidden layers and sigmoid activation function for the outer layer, resulted in the highest accuracy of 72.6%. This did not result in the targeted 75% but was very close. I would recommend acquiring more data so that other variables aside from 'IS_SUCCESSFUL' could provide more accuracy resulting in a better model. There would also be a benefit in using a Random Forest Classifier to better prevent overfitting and evaluating its performance against the current model. 
