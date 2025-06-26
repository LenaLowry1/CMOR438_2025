# The Neural Network Model

Now that we have made multiple models consisting of a single neuron, we will layer these neurons to produce a network. In such a model, the outputs of the previous layer become the inputs of the following layer. That means that the activation functions become increasingly composite as we move from layer to layer, until reaching the output vector.

![neural_ntwk.svg](neural_ntwk.svg)

# The Cost Function

# The Dataset

We will be using the [MNIST fashion dataset](https://keras.io/api/datasets/fashion_mnist/). This dataset includes low resolution images of 10 different kinds of clothing, indexed as below:

0   T-shirt/top
1	Trouser
2	Pullover
3	Dress
4	Coat
5	Sandal
6	Shirt
7	Sneaker
8	Bag
9	Ankle boot

While simliar in format to the MNIST digit dataset, these patterns and textures are more complex, presenting an additional challenge. 