# Project 3

### Using either the Classify structured data with feature columns script or the Classify structured data using Keras Preprocessing Layers with the country_persons.csv dataset, specify, train and evaluate models that predict class of wealth versus all other classes as a binary target. Amongst the five possible binary targets (1 versus all others, 2 versus all other etc...), produce your results from the two models with the best and worst accuracy.

#

To begin this project I started by using the preprocessing script and modifying it to predict each of the 5 wealth classes one at a time. By doing this it allowed me to compare which one models had the best and worst accuracies. I found that wealth class 2 had the worst accuracy at just under 75%, and wealth class 5 had the best accuracy at just over 95%.

## Wealth Classes 2 and 5 Accuracy Measurements:
![Screen Shot 2021-07-29 at 8 41 00 PM](https://user-images.githubusercontent.com/60228369/127586637-65085e49-4bdc-4cad-9173-26c9182a7ecd.png)
![Screen Shot 2021-07-29 at 8 39 08 PM](https://user-images.githubusercontent.com/60228369/127586643-b8cf1c06-93d4-477f-84d3-71f629b57841.png)


### Using the data and two models you produced in step 1, create a confusion matrix. You are welcome to use the following script. With your confusion matrix as a reference, analyze and discuss the two sets of results you produced.

# 

After I concluded that I would be using wealth classes 2 and 5 I continued to produce the confusion matrices using the provided script. I first used the preprocessing script to train the data again and I produced the following confusion matrices.

## Preprocessing Script Confusion Matrices:
![Screen Shot 2021-07-29 at 9 09 19 PM](https://user-images.githubusercontent.com/60228369/127586652-37f98ef8-99a7-411b-b3a0-10eb399db487.png)
![Screen Shot 2021-07-29 at 9 13 38 PM](https://user-images.githubusercontent.com/60228369/127586659-1fcf0593-3814-4364-a148-594b808d1cdc.png)



As you can see these matrices did not do very well. Each matrix simply predicted all values to have the label 0. What this means is that each matrix simply predicted that every value was not the wealth class (either 2 or 5) we were trying to predict. This result was not satisfactory to me so I decided to write a new script that was closer to the feature columns script than the previous one I had written using the preprocessing script. When writing this new script I also dropped some of the columns that I thought would not affect wealth class (these included the unit, pnmbr, hhid, size, and weights columns), and I categorized the remaining columns as either numeric or categorical columns. I then created these two new confusion matrices for wealth classes 2 and 5:

## Feature Columns Script Confusion Matrices:


These confusion matrices were more satisfactory to me. The first one I generated was for wealth class 2 and it did not change a lot. However, the second matrix I generated for wealth class 5 varied more from the preprocessing script confusion matrix. This satisfied me because I was now confident that I had written a script that was not simply predicting that the wealth class was not the set target. It also makes sense that the wealth class 5 matrix would vary more than the wealth class 2 matrix because at the beginning we calculated that wealth class 5 had the best accuracy after training. 


### Again using either the Classify structured data with feature columns script or the Classify structured data using Keras Preprocessing Layers with the country_persons.csv dataset, specify, train and evaluate a model that predicts all class of wealth outcomes as a categorical target. Again create a confusion matrix in order to analyze and discuss your results. Revisit the Classify structured data with feature columns script or the Classify structured data using Keras Preprocessing Layers in order to modify your feature columns, in an attempt to improve the accuracy of your model that uses all five categorical wealth classes as the target. Analyze and discuss your progress and results.

#

Finally, after finishing the confusion matrices for individual wealth classes I modified my feature columns script to predict all wealth classes from the other features. The first matrix fared okay and I was somewhat satisfied with the result.

## Confusion Matrix for all Wealth Classes.

However, after generating this matrix I decide that I wanted to see if I could modify the feature columns to improve the accuracy. To do this I decided to bucketize the age column and also use John's technique to bucketize the toilet column. These modifications resulted in the following matrix.

## Confusion Matrix with Modified Columns:


As you can see by comparing the two matrices the prediction results definitely changed by bucketizing certain feature columns. However, I found it interesting that while the predictions were different, it is hard to say if the matrix was more or less accurate. Some of the classes were predicted better with the bucketed columns and some were not. This result goes to show that when you wrangle 'wild data' the only way to really improve your results is often trial and error. I am sure there are countless possible modifications that can be made to the feature columns that change the confusion matrix predictions, and I am interested to look over what changes my classmates made, and whether or not these changes improved their accuracies. 
