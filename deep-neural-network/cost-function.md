# Cost vs Loss function

Loss is calculating a number based on a given loss function \(mean squared errors, stochastic gradient descent, adam, etc.\). The goal of 'training' a network is to find the combination of parameters that minimize the value calculated by that loss function. The number itself has little meaning in the absolute sense, but a decreasing loss number at every epoch is a good sign - it means the training is working.

Accuracy is a different concept.

Assume you've trained your model using a number of training examples, over 1 epoch or more, and you've seen the loss number decrease over time.

You now want to verify whether your model truly knows whether it can detect the objects you're training on. As your training adjusts the parameters of the neural net, it checks how many of the training inputs it is now classifying properly. Count the correct classifications, and divide by total, that's the accuracy.

You show it a new set of data that it has never seen before, you call that the "test set". You run that test set on your model, and count how many times it is predicting the correct label of the input, and how many times it's predicting a wrong label. The ratio of correct/\(total attempted\) is the accuracy of this validation pass.

### derivative of the _Loss_ function

which is a vector giving all the individual losses on each sample. .derivative of 

`dAL = - (np.divide(Y, AL) - np.divide(1 - Y, 1 - AL))`

### derivative of the _**Cost**_ function

which is the mean of the Losses across all samples, and thus is a scalar 

`dAL=-1/m*np.sum( (np.divide(Y, AL) - np.divide(1 - Y, 1 - AL))`

