# Decision Tree and Regression Tree Model

Decision Trees are non-parametric, supervised learning models used to make predictions based on learned decision rules derived from data features. Essentially, a decision tree makes inferences about what features are important in order to produce its classification rules. It produces a piecewise function, used to partition the data. The 'tree' works like a **directed graph** with the data flowing from the root node to a leaf representing its category.

![dec_tree.png](dec_tree.png)

They are popular because they:

- Are intuitive and easy to interpret
- Can handle both numerical and categorical data
- Work for both classification and regression problems
- Require minimal data preprocessing

Some disadvantages include:

- With too many layers, the model can **overfit** to the training data
- If data is rotated, it can lead to decreased performance, even if nothing else is changed
- Outliers can cause the boundaries to take on strange shapes

A decision/regression tree is composed of:

- Root Node: The starting point that splits the data based on a feature

- Decision Nodes: Intermediate nodes where further splitting occurs

- Leaf Nodes: Terminal nodes that hold the final prediction value

Each split is made to reduce impurity (e.g., gini score or squared error in regression) and improve the model’s ability to predict the target variable.

## The datasets

For the decision tree, we will use the [`make_circles`](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.make_circles.html) method to generate mock data. For the regression tree, we will use [`make_regression`](https://scikit-learn.org/0.15/modules/generated/sklearn.datasets.make_regression.html). Both are from [sklearn](https://scikit-learn.org/stable/).

## Packages

- [sklearn.metric](https://scikit-learn.org/stable/api/sklearn.metrics.html)
- [sklearn.tree](https://scikit-learn.org/stable/api/sklearn.tree.html)
- [sklearn.model_selection](https://scikit-learn.org/stable/api/sklearn.model_selection.html)