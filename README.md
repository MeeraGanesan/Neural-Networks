# Neural-Networks

Note: Code is kept private, can show on a need-to-know-basis.

This project implements an image recognition system using a neural network. 

The neural network classifies images using a single hidden layer. The data includes black and white images of the 4 classes: automobile, bird, frog, and ship. 

Model definition:

The neural network uses a sigmoid activation function for the hidden layer, and a softmax on the output layer. The output layer is a probability distribution over the 4 classes. So, each element in the output vector represents the probability that the input vector x belongs to that particular class. There are 2 types of initialization possible:
1. Random: The weights are initialized randomly from a uniform distribution from -0.1 to +0.1. The bias parameters are set to 0
2. Zero: All weights are initialized to 0.
The desired initialization is set via a command line flag.

The learning rate is set via a command line flag.

The objective function used to train the model is average cross entropy over the training dataset. The objective function is optimized using Adagrad, a variant of SGD (Stochastic Gradient Descent). The number of epochs can be specified as a command line flag.

The label assigned to an image is the class corresponding to the maximum probability in the output vector.
