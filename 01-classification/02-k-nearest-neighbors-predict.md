# 02-k-Nearest Neighbors: Predict

k-Nearest Neighbors: Predict

Having fit a k-NN classifier, you can now use it to predict the label of a new data point. However, there is no unlabeled data available since all of it was used to fit the model! You can still use the .predict\(\) method on the X that was used to fit the model, but it is not a good indicator of the model's ability to generalize to new, unseen data.

In the next video, Hugo will discuss a solution to this problem. For now, a random unlabeled data point has been generated and is available to you as X\_new. You will use your classifier to predict the label for this new data point, as well as on the training data X that the model has already seen. Using .predict\(\) on X\_new will generate 1 prediction, while using it on X will generate 435 predictions: 1 for each sample.

The DataFrame has been pre-loaded as df. This time, you will create the feature array X and target variable array y yourself.

### Import KNeighborsClassifier from sklearn.neighbors

`from sklearn.neighbors import KNeighborsClassifier`

### Create arrays for the features and the response variable

`y = df['party'].values X = df.drop('party', axis=1).values`

### Create a k-NN classifier with 6 neighbors: knn

`knn = knn = KNeighborsClassifier(n_neighbors=6)`

### Fit the classifier to the data

`knn.fit(X,y)`

### Predict the labels for the training data X

y\_pred = knn.predict\(X\)

### Predict and print the label for the new data point X\_new

new\_prediction = knn.predict\(X\_new\) print\("Prediction: {}".format\(new\_prediction\)\)

### Measuring model performance

in classification, accuracy is a commonly used metric

Accuracy = \# of correct predictions/Total number of data points

Which data do we use to compute accuracy? What we are really interested in is how well our model performs on new data. that is samples that the algorithm has never seen before. If we use the training data-set, that would not be a good classifier as this was seen by the model already. 

So the common practice is to split our data in two sets. A training set and a test set and:

1. fit/train the classifier on the training set
2. make predication on the test set
3. compare the predication with the known labels

Lets take a look at the code:

1. We first import the train test split from sklearn dot model selection
2. use the train test split function to randomly split our data
3. the first argument **`'X'`** is our feature data, the 2nd target or labels **`'y'`**
4. **`test_size`** keyword argument specifies what proportion of the original data is used for the test set.
5. **`random_state kwarg`** set a seed for the random number generator that splits the data into train and test which splits the data in to train and test. Setting the seed with the same argument later will allow you to reproduce the exact split and your downstream results.
6. train\_set\_split returns 4 arrays:

   1. training data
   2. test data
   3. training labels
   4. test labels

7. Next we unpack these into 4 variables of **`X_train, X_test, y_train, y_test.`** 
8. By default train\_test\_split, splits data into 75% training and 25% test data which is a good rule of thumb. Here we specify our size of split using the test\_size to 30%.
9. It is also best practice to perform your split so that the split reflect the labels on your data. That is you want your labels to be distributed in train and test sets as they are in the original data-set. To achieve this we use the keyword argument stratify equals y, where y is the list or array containing the labels.
10. Next we instantiate our k-nearest neighbors classifier, 
11. fit it to the training data
12. make our prediction using the test data and store the result in **`y_pred`**, printing them shown 3 values as expected.
13. To check out the accuracy of our model we use the score method of the model and pass the **`X_test and y_test.`**

**`Note:`**As K increases, the decision boundary gets smoother  and less curvy.

![](../.gitbook/assets/image%20%281%29.png)

Larger K = smoother decision boundary - less complex model

Smaller K = More complex model = can lead to over fitting

![](../.gitbook/assets/image%20%282%29.png)

### 

### Model complexity curve \(over/under-fitting\)

Below you can see that there is a sweet spot in the middle that can give us the best performance on the test set.

![](../.gitbook/assets/image%20%283%29.png)









  


