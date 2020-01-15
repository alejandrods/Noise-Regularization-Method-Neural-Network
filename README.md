# Noise: It is not always annoying
### Adding noise as regularization method to reduce overffiting in neural networks

One of the first concepts you learn when you are beginning to study neural networks is the meaning of overfitting or underfitting. Many times, it is a challenge to train a model that generalize perfectly your data, especially when you have a small dataset because:

- When you train a neural network with small datasets, generally the network memorizes the training dataset instead of learning general features of our data. For this reason, the model will perform well on the training set and poor on new data (for instance: the test dataset)

- A small dataset provides a poor description of our problem and thus, it may result in a difficult problem to learn.

To acquire more data it is a very expensive and arduous task. However, sometimes you can apply some techniques (regularization methods) to get a better performance in your model.

In this talk, we are focusing on the use of noise as a regularizing method in a neural network. This technique not only reduces overfitting, but it can also lead to faster optimization of our model and better overall performance.

You can find the entire code in [Medium](https://medium.com/@alejandrods)! :)

## Goals

The objectives of this talk are the following:
- Generate synthetic data using sklearn.
- Train a basic Neural Network as a baseline.
- Use noise as regularization method - input layer
- Use noise as regularization method - hidden layer
- Use noise as regularization method - input and hidden layer
- Grid Search to find the values for the best performance of the model.

Additionally, we will learn to create a grid to evaluate many points at the same time and check how our model classifies these points plotting a heat-map.
