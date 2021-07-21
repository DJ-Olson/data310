# Iris Dataset Writeup
## Using the Custom training: walkthrough script we developed during today's class, write a 1-1/2 to 2-page report that provides a description of the following.

### Describe the data used in the model

The data used in this exercise is the Iris flower dataset from TensorFlow. It is a multivariate dataset that was first introduced in Ronald Fisher, a British statistician’s, 1936  paper. The dataset comprises three species of Iris: Iris setosa, Iris virginica and Iris versicolor. Fifty samples of each of the species were collected and four features were measured on each sample, the length of the sepals, the width of the centimeters, the length of the petals, and the width of the petals. These four features were collected with the goal of being able to distinguish the three species from each other. 

#

### How the tf.dataset was created:

A TensorFlow dataset is created by following three steps. The first is picking a source dataset and importing it into a python environment. Then an iterator needs to be created to iterate through the dataset. Finally the data needs to be consumed. This is done by using the iterator to pull out elements from the dataset and feed them back into the model. 

#

### How the model architecture was specified:


The model architecture was constructed using the following code:


This code specifies that we want the model to have 3 dense layers. The first two layers had 10 neurons each and the last had 3. The input_shape(4) portion of the code is included because each data point has four feature values that were previously mentioned. 

#

### How the model was trained

To train the model we had to develop a loss function. Because the target values of this model were not numeric values we had to use a loss function to find the SparseCategoricalCrossEntropy loss. The goal of the model was to predict a categorical label for the species of Iris based on the feature data. Because of this we had to use one hot label encoding to encode the target  labels, and then assign them numeric values between 0-2. This made the model able to predict a numeric value that was then converted to one of the three possible species labels (Iris setosa, Iris virginica and Iris versicolor). 

#

### How the model was optimized:

During the training portion of the model is also when the data is gradually optimized. To optimize our model we used the following code:


The command tf.GradientTape() is used to calculate the gradients used to optimize the model. An optimizer applies gradients to a model in order to minimize the loss function. Gradients do this by finding the point of greatest ascent in the model. Because we want to minimize the difference between the predicted and actual label in this model, we then travel the opposite direction of the point of greatest ascent. In this dataset we used a stochastic gradient descent (SGD) algorithm to optimize the model. We created a loop for this algorithm so that the stochastic gradient descent could be applied over and over again and hopefully decrease the loss of the model as much as possible. 

#

### How the loss was estimated:

To estimate the loss we trained the model over 200 epochs. This is not a lot of epochs to the model trained quickly and resulted in an accuracy of 99.167% on the 200th epoch which indicates we have a good model. Below is a plot that describes that change per epoch:

#

### How the model was evaluated with test data:

To evaluate our model we loaded in a new Iris test dataset so we could use data that the model had not been trained on. We then used the tf.keras.metrics.Accuracy() function to test the accuracy of the model with the new data by comparing the predicted label values to the actual label values. The resulting accuracy for the test dataset was 96.667% It makes sense that it was not as high as the dataset we used to train the model, however, this is still a high accuracy that indicates our model is good.


#

### How new predicitons are able to be made:
 
We can also use this model to make predictions on unlabeled Irises. This is done by manually creating a new dataset with only feature information but no labels. The model can take the feature information and then predict a label name (species of Iris), while also telling you how confident it is in its prediction with a percentage indication. 

