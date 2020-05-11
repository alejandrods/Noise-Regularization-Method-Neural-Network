# Noise: It's not always annoying
### Adding noise as regularization method to reduce overffiting in neural networks

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1P71Q7-C08yTlvwbI4tNJWTnkYbJyXSID)

One of the first concepts you learn when you are beginning to study neural networks is the meaning of overfitting or underfitting. Many times, it is a challenge to train a model that generalize perfectly your data, especially when you have a small dataset because:

- When you train a neural network with small datasets, generally the network memorizes the training dataset instead of learning general features of our data. For this reason, the model will perform well on the training set and poor on new data (for instance: the test dataset)

- A small dataset provides a poor description of our problem and thus, it may result in a difficult problem to learn.

To acquire more data it is a very expensive and arduous task. However, sometimes you can apply some techniques (regularization methods) to get a better performance in your model.

In this talk, we are focusing on the use of noise as a regularizing method in a neural network. This technique not only reduces overfitting, but it can also lead to faster optimization of our model and better overall performance.

You can find the entire article in [Medium](https://medium.com/@alejandrods)! :)

## Goals

The objectives of this talk are the following:
- Generate synthetic data using sklearn
- Regularization Methods
- Train a basic Neural Network as a baseline
- Use noise as regularization method - input layer
- Use noise as regularization method - hidden layer
- Use noise as regularization method - input and hidden layer
- Grid Search to find the values for the best performance of the model

Additionally, we will learn to create a grid to evaluate many points at the same time and check how our model classifies these points plotting a heat-map.

## Regularization Methods

It is a challenge to train a machine learning model that will perform well on previously unseen inputs, not just those on which our model was trained. This feature is called [generalization](https://books.google.es/books?id=Np9SDQAAQBAJ&pg=PA107&lpg=PA107&dq=The+central+challenge+in+machine+learning+is+that+our+algorithm+must+perform+well+on+...&source=bl&ots=kROllLy-_Z&sig=ACfU3U1FzdT_Vg1GkcsBupzbmt8YHWQvhw&hl=es&sa=X&ved=2ahUKEwiph6T22YfnAhW9DWMBHVkNDkgQ6AEwAHoECAwQAQ#v=onepage&q=The%20central%20challenge%20in%20machine%20learning%20is%20that%20our%20algorithm%20must%20perform%20well%20on%20...&f=false), performs well on unobserved inputs. There are some methods like train-test split or cross-validation to measure how well generalize our model. 

We can classify the performance of the model in 3 cases:
- The model performs poorly on the training dataset and new data - Underfit Model.
- The model performs well on the training dataset and poorly on unseen data - Overfit Model.
- The model learns our training dataset and performs well on unseen data, it is capable to generalize - Good Fit Model

It is more likely to face overfitting models in our problems thus, it is important to monitor the performance during training to detect if it has overfitting. It is common to plot the evolution of accuracy and loss during the training to detect usual patterns.

![performance_model](/image/performance.png "Underfit, Good-fit, Overfitting")

[Regularization](https://towardsdatascience.com/regularization-in-machine-learning-76441ddcf99a) is to modify our learning algorithm to reduce its generalization error but not its training error. The most common regularization methods in neural networks are:
- Dropout: Turn on some neuron in each iteration with probability p.
- Early Stopping: Provide guidance as to how many iterations can be run before the model begins to overfit.
- Weight Constraint: Scales weights to a pre-defined threshold.
- Noise: Introduce stochastic noise into training process.

These methods are popular in neural networks and most of them have been proven to reduce overfitting. However, the effect of noise on deep learning models has never been systematically studied, nor is the underlying reason for the improved accuracy. [One hypothesis of the above observation is that relaxing consistency introduces stochastic noise into training process.](https://pdfs.semanticscholar.org/d79b/a428e1cf1b8aa5d320a93166315bb30b4765.pdf) This implicitly mitigates the overfitting of the model and generalizes the model better to classify test data.

## Future Experiments
- We can improve this experiment of adding noise as regularization method with the next ideas:
- Add more layers with noise to study his effect.
– Repeat the same experiments with a deeper neural network.
- Study the effect of noise as a regularization method in a model without overfitting.
- Try to add noise to activations, weights and outputs.

Suggestions and reviews are welcome. Follow me and thank you for reading! :)
