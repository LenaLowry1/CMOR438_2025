# The Logistic Regression Model

Similar to the perceptron and linear regression model, the logistic regression model is also constructed from a single neuron. In this file, we will focus on the important changes to the linear regression model in order to produce the logistic regression model.

![linear_vs_logistic.png](linear_vs_logistic.png)

## The differences

Most importantly, the logistic function is similiar to the perceptron in that it performs **binary classification**. However, it is unique because while the perceptron simply makes a classification, the logistic model will output a conditional probability- namely the probability that an input belongs belongs in a class, given the measurements in its input vector. The probability can still lead to a classification, but the programmer must set a threshold (typically 0.5), so that inputs with probabilities below the threshold belong to one class, and those with probabilities that are higher belong to another.


New activiaiton function: $$\sigma(z) = \frac{1}{1 + e^{-z}}$$
The sigmoid activation function is used in logistic regression because it maps any real-valued number into the interval (0, 1), making it ideal for representing probabilities. Additionally, the smooth S-shape makes the function continuous and differentiable.

Finally, we need a new loss function. For this model, we utilize the binary cross entropy loss function. The concept behind this choice is the maxmimization of the sum over all of the data of the following conditional probability: 
<<<<<<< HEAD
$$
P\Big(y^{(i)}\mid x^{(i)}\Big)=\begin{cases}
          \hat{y}^{(i)}, \quad &  y^{(i)} = 1 \\
          1-\hat{y}^{(i)}, \quad & y^{(i)} = 0 \\
     \end{cases}
$$
=======
P(y⁽ⁱ⁾ | x⁽ⁱ⁾) = { ŷ⁽ⁱ⁾, if y⁽ⁱ⁾ = 1 & 1 - ŷ⁽ⁱ⁾, if y⁽ⁱ⁾ = 0}

>>>>>>> 12a8fc7cff988a7751bc60aa9f33c6405a92c7b1

The "more correct" our probability is (i.e., the closer it is to the true value of the data point), the larger this sum will be. Thus, at the maximum of this sum, we will find the weights and bias term that best classify the data.
After applying the Bernoulli formula and using log rules to simplify the expression, we are left with: 

<<<<<<< HEAD
$$\begin{align} 
\log \Big(y^{(i)}\mid x^{(i)}\Big)&= y\log \hat{y} + (1-y) \log (1 - \hat{y})\\ 
\end{align}$$
=======
log P(y⁽ⁱ⁾ | x⁽ⁱ⁾) = y log(ŷ) + (1 - y) log(1 - ŷ)
>>>>>>> 12a8fc7cff988a7751bc60aa9f33c6405a92c7b1

Since the log function is monotonically increasing, the point at which it is maxmized is also the point at which the orignial conditional probability is maximized.
Now, fully expressing the loss function in terms of w and b, and dividing my N in order to find the **average** error gives: 

L(w, b) = (1 / N) ∑ᵢ [ −y⁽ⁱ⁾ log(ŷ⁽ⁱ⁾) − (1 − y⁽ⁱ⁾) log(1 − ŷ⁽ⁱ⁾) ]



Note that we are minimizing the **negative** of this function, which is the same as maximizing the positive. This enables us to consistently use gradient descent.

## The dataset

Again we will use the "penguins" dataset, focusing on the Adelie and Chinstrap penguins, as their data is not linearly separable, as shown in the Perceptron model.
