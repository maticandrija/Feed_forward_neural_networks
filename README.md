# Feed_forward_neural_networks

###In this project I would lead you through implementation of Feedforward Neural Network for solving one of the most known regression projects, Californa housing.

###Feedforward Neural Network

A feedforward neural network (FNN) is one of the two broad types of artificial neural network, characterized by direction of the flow of information between its layers. Its flow is uni-directional, meaning that the information in the model flows in only one direction—forward—from the input nodes, through the hidden nodes and to the output nodes, without any cycles or loops. Modern feedforward networks are trained using the backpropagation method and are colloquially referred to as the "vanilla" neural networks.

Activation function used in this project, [`rectified linear unit (ReLU) function`](https://en.wikipedia.org/wiki/Ramp_function) (also known as the `ramp or hinge function`) $f: \mathbb{R} \mapsto [0,\infty)$ is a piecewise linear function defined as:

\begin{align}
f(x) := \max (0,x) = x\mathbf{1}_{\{x>0\}} = \begin{cases}
           x, & \text{if $x>0$}\\
           0, & \text{otherwise}.
	   \end{cases}
\end{align}

The first-order derivative is zero for $x < 0$, one for $x>0$, and it is not defined for $x=0$.

The standard ReLU function is a kink-shaped function which is constructed by mixing the identity and the binary step function. It is one of the most commonly used activation functions for hidden layers due to the following characteristics:
* `Simplicity and easy implementation` since it is piecewise linear function,
* `Representational sparcity` (i.e., the property of giving zero as the output) which improves the computational speed,
* `Improved convergence` over other popular activation function such as the sigmoid and hyperbolic tangent functions (e.g., the vanishing gradient problem).

For optimizer purposes, I've used **kerras optimizer** with **Adam** and **Stohastic Gradient Descent** (SGD) as optimization function.

In later part of the project, hyperparameters optimization will focus on two parameters,

*   epochs
*   batch_size


Epochs will take values from 50 to 500 with values [50, 100, 250,500].

Batch_size will take values from 32 to 256 with progressive step of power of 2.
