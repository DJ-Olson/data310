# Iris and Metro Dataset Preprocessing and Training

## Below are the plots of the two datasets preprocessing steps. 

## Iris 
![Screen Shot 2021-07-23 at 4 27 12 PM](https://user-images.githubusercontent.com/60228369/126841726-07dbfe21-4af4-456b-9b78-9c6fd68d3df1.png)

## Metro
![Screen Shot 2021-07-23 at 4 26 56 PM](https://user-images.githubusercontent.com/60228369/126841728-96430ccb-74a1-4cf4-801b-7661233bdd63.png)

### What does each box in the illustration represent?
Each box represents a preprocessing layer.

### Are there different paths towards the final concatenation step? What is occurring at each step and why is it necessary to execute before fitting your model. 

The Metro dataset has many more layers than the Iris dataset. This is because the iris dataset has only numeric features, and the plot above shows that all four of them are immediately concatenated into one layer. Whereas the Metro dataset had four numeric features and four categorical features. In both datasets the numeric features were concatenated together and then normalized. However, in the Metro dataset the categorical features needed to use 'one hot' string lookup and then use category encoding before they could be concatenated with the normalized numeric features from the Metro dataset. In summary, the Iris dataset was much simpler because it only had one type of feature, and thus, less preprocessing layers were needed to reach the final concatenation step.

## Below are the calculated losses of each dataset

## Iris
![Screen Shot 2021-07-23 at 4 48 07 PM](https://user-images.githubusercontent.com/60228369/126841733-a45c3399-9a2f-4b66-b445-33797b20c309.png)

## Metro
![Screen Shot 2021-07-23 at 4 26 21 PM](https://user-images.githubusercontent.com/60228369/126841739-3e912f87-50bf-4c74-bb11-fa0f3e7c2215.png)

### Train each model and produce the output (not necessary to validate or test). Describe the model output from both the metro traffic interstate dataset and the iris flowers dataset. What is the target for each dataset? How would you assess the accuracy of each model? Are you using a different metric for each one? Why is this so? What is each one measuring?
The loss for the Iris dataset is much better than the massive loss from the Metro dataset. I would assume this is because the Iris dataset is much simpler, and likely much easier to train. The target for the Iris dataset is 'species', and for the Metro dataset the target is 'traffic_volume.' You can assess the accuracy of each model by looking at the loss values. The Iris dataset is definitely more accurate. The metric we are using to assess the Metro dataset is mean squared error. We used this to assess traffic volume because we can measure a number of cars. For the Iris dataset we used binary cross entropy, because we are measuring whether a given flower is a species of iris or not. 





