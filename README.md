# ATM_Camera
We are tasked with making a smart ATM camera which can distinguish between dollar notes and checks.We want to make sure that dollars are not classified as checks, and that checks are not classified as dollars.

We are given a set of 87 images of checks and dollars, each of which have been scaled to 322 X 137 pixels, and where each pixel has 3 color channels.
### Part 1
#### Data Collection
Data is provided in the data folder and its path is already set in the file.We upload the data to the pandas dataframe so that we can easily handle that data.
### Part 2
#### Exploring the data
We explore the pictures of the checks and dollars to figure out the differences visually.We noticed that the each data has large no. of features which is quite a big problem.
### Part 3
#### Feature Engineering
To solve the problem of this high dimensionality of the dataset we use an unsupervised learning method called PCA(Principal Component Analysis).We do PCA transformation on this data set which is a fancy way to say that we will try to reduce the dimensionality of this data set.After PCA we reduce the features to 60 features which is far less than the no. of features we had before.
### Part 4
#### Classification
For the classification, we will use the KNN(k-Nearest Neighbour) method.This technique of classification is present in the sklearn library.We just use that algorithm to classify that data set.We spit this data set into two parts-Test set and train set, so that we can check the accuracy of our model with the help of test data set.When we do classification we see overfiitting in our model.To remove overfitting of the train data we used Cross-Validation.Cross-validation solved the overfitting problem with the model and then we are left with a model whose both test and train accuracy are 94%.To measure the score of our classifier we used accuracy score and confusion metrics.
