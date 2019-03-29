# Cost vs Loss function

### derivative of the _Loss_ function

which is a vector giving all the individual losses on each sample. .derivative of 

`dAL = - (np.divide(Y, AL) - np.divide(1 - Y, 1 - AL))`

### derivative of the _**Cost**_ function

which is the mean of the Losses across all samples, and thus is a scalar 

`dAL=-1/m*np.sum( (np.divide(Y, AL) - np.divide(1 - Y, 1 - AL))`

