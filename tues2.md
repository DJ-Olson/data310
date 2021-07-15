# Higgs Dataset and Image Processing Responses

# Part 1 (Higgs Dataset)

## Question 1 
### Describe the dataset. What type of variable is the target? How many features are being used? How many observations are in the training dataset? How many are used in the validation set?

#
The Higgs Dataset is a dataset relating to particle physics that contains 11 million examples. The target in this dataset is a continuos variable. Within the dataset there are 28 features used. The training dataset uses 10,000 obseravations, and the validation set uses 1,000 observations. 

## Question 2
### How did each of the four models perform (tiny, small, medium and large)? Which of the four models performed the best? Which ones performed the worst? Why in your estimation did certain models perform better? Produce a plot that illustrates and compares all four models.

![Screen Shot 2021-07-14 at 5 01 55 PM](https://user-images.githubusercontent.com/60228369/125692930-ac32217a-bc17-466f-b005-cdbb0606f597.png)

#
The graph above demonstrates the performance of each of the models. The tiny model performed the best and the small model performed alright. You can tell the tiny model performed the best because the training and validation values depicted by the lines are very similar. The small model performed alright, but you can tell it was close to overfitting because the validation line began to go constant while the training line was still moving. Both the medium and large models performed the worst. You can see this in the graph above because the training and validation lines are moving in opposite directions. I think that the smaller models performed better than the larger models because it is easier to train a model with less parameters. 


## Question 3
### Apply regularization, then add a drop out layer and finally combine both regularization with a dropout layer. Produce a plot that illustrates and compares all four models. Why in your estimation did certain models perform better?

#
The graph above shows that the combined (L2 and dropout) performed best. I think this is because it added weight penalties to the models loss while at the same time dropping out features as the model trained. 

## Question 4
### What is an overfit model? Why is it important to address it? What are four different ways we have addressed an overfit model thus far?

#
An overfit model is a model that is trained by a certain set of points too much. This means that when new data is introduced, the training model and the test model are not very similar. It is important to address overfitting because when you are using a model that you want to implement new data to, the model will not be affectivley trained if it is overfit. The four ways we have learned to address overfit models so far are: L1 regularization, L2 regularization, dropout model, and L2 combined with dropout model. 
