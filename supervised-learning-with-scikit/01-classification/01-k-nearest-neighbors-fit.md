# 01-k-nearest-neighbors-fit

k-Nearest Neighbors: Fit

K-nearest neighbors \(KNN\) classification

1. pick a value for K \(like 5\)
2. search for the K \(5\) observation in the training data that are "nearest" to the measurement of the unknown iris for example
3. use the most popular response value from the K nearest neighbours as the predicted response value for the unknown iris.

So basically the model searches for the 5 observations in the training data that are nearest to the measurements of the unknown iris in other words the model calculates the numerical distance between the unknown iris and each of the 150 known irises and selects the five known irises with the smallest distance to the unknown iris note that Euclidean distance is often used as the distance metric but other metrics can be used instead, third the response values of the five nearest neighbors are tallied and whichever response value is the most popular is used as the predicted response value for the unknown iris.

Having explored the Congressional voting records dataset, it is time now to build your first classifier. In this exercise, you will fit a k-Nearest Neighbours classifier to the voting dataset, which has once again been pre-loaded for you into a DataFrame df. In the video, Hugo discussed the importance of ensuring your data adheres to the format required by the scikit-learn API. The features need to be in an array where each column is a feature and each row a different observation or data point - in this case, a Congressman's voting record. The target needs to be a single column with the same number of observations as the feature data. We have done this for you in this exercise. Notice we named the feature array X and response variable y: This is in accordance with the common scikit-learn practice. Your job is to create an instance of a k-NN classifier with 6 neighbours \(by specifying the n\_neighbours parameter\) and then fit it to the data. The data has been pre-loaded into a DataFrame called df.

What the K-NN algorithm essentially does is that it creates a set of decision boundaries.

![k-nn intuition: Creating decision boundries](../../.gitbook/assets/image%20%2811%29.png)





INSTRUCTIONS:

Note the use of .drop\(\) to drop the target variable 'party' from the feature array X as well as the use of the .values attribute to ensure X and y are NumPy arrays. Without using .values, X and y are a DataFrame and Series respectively; the scikit-learn API will accept them in this form also as long as they are of the right shape.

## Import KNeighborsClassifier from sklearn.neighbors

`from sklearn.neighbors import KNeighborsClassifier`

## Create arrays for the features and the response variable

`y = df['party'].values   
X = df.drop('party', axis=1).values`

## Create a k-NN classifier with 6 neighbors

`knn = KNeighborsClassifier(n_neighbors=6)`

## Fit `(training)`the classifier to the data

`knn.fit(X,y)`

**`When we say training a model on the data, it's same as 'fitting' a model to the data`** 





