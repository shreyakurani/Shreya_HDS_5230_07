## Neural Network Type Chosen: Feed-Forward Neural Network (FFNN)

Feed forward neural network (FFNN) is one of the simplest and basic types of neural networks. 
The name is ‘feed forward’ because the data flows in one direction: from the input layer to the hidden layers to the output with no cycles or loops.
Inputs are received by each node (or neuron), weighted sum applied, passed through an activation function (say, ReLU, monotone sigmoid or anything else) and the result is forwarded to the following layer. 
It adjusts its weights with gradients using the backpropagation method and gradient descent in order to minimize the loss in the network during the training.

## FFNNs are often used in:-

1. Classification tasks such as medical diagnosis, spam detection, etc.

2. Regression problems (e.g., house price prediction)

3. Any task with structured/tabular input data

## These models work best when:-

1. The input features are independent and numerical.

2. Data is preprocessed (scaled, normalised)

However, FFNNS aren’t great at sequence data — an RNN or LSTM is a better choice.
The problem is that FFNNs are very sensitive to scaling, overfit particularly easily with too complex model when has a small data set.

## What I did:- 
For this assignment, I created FFNNs with 1 and 2 hidden layers using synthetic datasets and trained them. 
I varied the size of the dataset and performed similar experiment against XGBoost.

The notebook linked below has a full implementation.
(https://github.com/shreyakurani/Shreya_HDS_5230_07/blob/main/Week_12/Week12_DeepLearning_Comparison_Extra_Credit.ipynb)
