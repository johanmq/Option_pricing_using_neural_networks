## Last version with notable improvements to come soon ##

In this notebook we design simple neural networks from scratch in order to compute European call price.

We use the Black & Scholes framework and we use the closed form solution provided by the model as a benchmark for training/evaluating our networks.

We will see that the activation function choice has a big impact on network performance. Sigmoid function does not perform well for deep in the money calls. RELU function performs better but lacks of regularity/smoothing. Finally, good performance are obtained using ELU functions.

This project was conducted by Johan Macq during ENSAE Master 2 year.

Several tests has shown that a learning rate of 0.01 as well as 4 hidden layers with 20 units in each is optimal for our networks.
