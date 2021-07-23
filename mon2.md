# Iris and Metro Dataset Preprocessing and Training

## Below are the plots of the two datasets preprocessing steps. 

## Iris 

## Metro


### What does each box in the illustration represent?
Each box represents a preprocessing layer.

### Are there different paths towards the final concatenation step? What is occurring at each step and why is it necessary to execute before fitting your model. 

The Metro dataset has many more layers than the Iris dataset. This is because the iris dataset has only numeric features, and the plot above shows that all four of them are immediately concatenated into one layer. Whereas the Metro dataset had four numeric features and four categorical features. In both datasets the numeric features were concatenated together and then normalized. However, in the Metro dataset the categorical features needed to use 'one hot' string lookup and then use category encoding before they could be concatenated with the normalized numeric features from the Metro dataset. In summary, the Iris dataset was much simpler because it only had one type of feature, and thus, less preprocessing layers were needed to reach the final concatenation step.

## Below are the calculated losses of each dataset

## Iris

## Metro


### Train each model and produce the output (not necessary to validate or test). Describe the model output from both the metro traffic interstate dataset and the iris flowers dataset. What is the target for each dataset? How would you assess the accuracy of each model? Are you using a different metric for each one? Why is this so? What is each one measuring?
The loss for the Iris dataset is much better than the massive loss from the Metro dataset. I would assume this is because the Iris dataset is much simpler, and likely much easier to train. The target for the Iris dataset is 'species', and for the Metro dataset the target is 'traffic_volume.' You can assess the accuracy of each model by looking at the loss values. The Iris dataset is definitely more accurate. The metric we are using to assess the Metro dataset is mean squared error. We used this to assess traffic volume because we can measure a number of cars. For the Iris dataset we used binary cross entropy, because we are measuring whether a given flower is a species of iris or not. 



