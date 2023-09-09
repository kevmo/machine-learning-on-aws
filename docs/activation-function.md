An activation function is a crucial component in neural networks, particularly in artificial neurons. It's used to determine the output of a neuron based on a given set of inputs. The activation function takes the weighted sum of the inputs and produces an output signal which is then used as input to the next layer in the neural network.

**The primary purpose of an activation function is to introduce non-linearity into the network. Without non-linearity, no matter how many layers our neural network has, it would behave just like a single-layer perceptron because summing these layers would give another linear function. A non-linear activation function allows the neural network to capture complex mappings between its inputs and outputs, making it possible for the network to learn from error and adjust its weights in the presence of complex data and patterns.

Here are some commonly used activation functions:

1. **Sigmoid or Logistic**:\[ f(x) = \frac{1}{1 + e^{-x}} \]Produces outputs between 0 and 1. It's historically popular but can lead to vanishing gradient problems in deep networks.
2. **Hyperbolic Tangent (tanh)**:\[ f(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}} \]Produces outputs between -1 and 1, thus centered at zero. Like the sigmoid, it can also lead to vanishing gradient problems in deep networks.
3. **Rectified Linear Unit (ReLU)**:\[ f(x) = \max(0, x) \]It gives an output x if x is positive and 0 otherwise. It's computationally efficient and helps mitigate the vanishing gradient problem, but it can suffer from "dead neurons" where neurons can sometimes be stuck during training and not update their weights (known as the dying ReLU problem).
4. **Leaky ReLU**:Introduces a small slope to keep the updates alive. Instead of the function being zero when x < 0, a leaky ReLU allows a small, non-zero gradient which avoids the dying ReLU problem.
5. **Softmax**:
   Often used in the output layer of a classifier where we're trying to attain probabilities for multiple classes. The softmax function can take an input vector and transform it into a probability distribution.

In deep learning, the choice of activation function can greatly influence the performance of the model. Different functions have different characteristics and can influence the model in different ways, like how quickly the model can learn, the likelihood of getting stuck during training, and the ability of the network to handle non-linearities in the data.
