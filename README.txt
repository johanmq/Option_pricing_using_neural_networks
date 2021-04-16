In this notebook we design simple neural networks from scratch in order to compute European call price. We use the Black & Scholes framework and we use the closed form solution provided by the model as a benchmark for training/evaluating our networks.

We will see that the activation function choice has a big impact on network performance. Sigmoid function does not perform well. RELU function performs better but lacks of regularity/smoothing that can be partially fixed with a higher number of layers. ELU function is more smooth that RELU but its negative part leads so significant error when time to maturity is short.

We note that the use of time to maturity as a parameter (instead of time alone) has helped to improve networks performances significantly. Instead of pricing the call price directly we price the time value, because the intrinsic value is deterministic and the payoff is then capped with ATM time value.

Several tests has shown that a learning rate of 0.05 as well as 6 hidden layers with 30 units in each allows to reach good performance. However, as the point here was to build a simple network from scratch we did not test advanced features as dropout, etc.

Overall perfomance is quite good, time value is well predicted for almost every maturity. Difficulties arise when the time to marutity becomes very short (less than 0.05) due to strong variations of time value (strong second orders greeks).
