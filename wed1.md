# Wednesday Responses

## 1) 
Below are 3 new images from the 'preprocess the data' section of the dataset:

1. ![Screen Shot 2021-07-07 at 9 38 24 PM](https://user-images.githubusercontent.com/60228369/125006211-97354b80-e02b-11eb-9c3a-17681b45d13d.png)

2. ![Screen Shot 2021-07-07 at 9 38 34 PM](https://user-images.githubusercontent.com/60228369/125006213-98667880-e02b-11eb-8647-b9e149ce31a2.png)

3. ![Screen Shot 2021-07-07 at 9 38 12 PM](https://user-images.githubusercontent.com/60228369/125006218-9997a580-e02b-11eb-9ff7-5f79b16fd0a7.png)

## 2) 
The array below from the 'make predictions' section represents a list of probabilities corresponding to each of the 10 different image classes we specified. The softmax function transform an array of normal numbers in probabilities between 0 and 1 that sum to 1. In this case it appears that the second value in the array shows that the software is nearly 100% confident that the image should be classified in image class 1, which corresponds to a trouser. The argmax function for this image produces the value 1, also corresponding to the image class trouser.

![Screen Shot 2021-07-07 at 9 43 36 PM](https://user-images.githubusercontent.com/60228369/125006996-5f2f0800-e02d-11eb-92b1-f938f440c5cf.png)


## 3) 
Below are 2 new images from the 'verify predictions' section of the dataset:

1. ![Screen Shot 2021-07-07 at 9 49 08 PM](https://user-images.githubusercontent.com/60228369/125007254-d795c900-e02d-11eb-886d-90cf3ab9e519.png)

2. ![Screen Shot 2021-07-07 at 9 49 21 PM](https://user-images.githubusercontent.com/60228369/125007255-d795c900-e02d-11eb-826a-be68ad742299.png)

## 4) 
The image below from the 'train model' section of the data shows that the model predicted the image was an ankle boot. This matches the label '9' that was produced by the argmax function. We did not use the softmax function in this case because we simply wanted the label from the different classes which run sequentially 0-9, and did not want to see the probabilities that the image was each of the classes. These probabilites were calcualted by the following code: 

predictions_single = probability_model.predict(img)


1. ![Screen Shot 2021-07-07 at 9 54 42 PM](https://user-images.githubusercontent.com/60228369/125007796-10826d80-e02f-11eb-94e7-764a55438fb9.png)


## 5)
Below is a plot of 25 handwritten numbers from the new mnist dataset with their labels indicated below each image. The accuracy of the test dataset and training dataset are also included.

1. ![Screen Shot 2021-07-07 at 10 01 16 PM](https://user-images.githubusercontent.com/60228369/125007954-740c9b00-e02f-11eb-9d3c-49026611c27f.png)

2. ![Screen Shot 2021-07-07 at 10 03 27 PM](https://user-images.githubusercontent.com/60228369/125007977-7e2e9980-e02f-11eb-9d39-d2e33d4bd50f.png)

3. ![Screen Shot 2021-07-07 at 10 03 10 PM](https://user-images.githubusercontent.com/60228369/125007978-7e2e9980-e02f-11eb-8b6f-39b38103efb8.png)

## 6) 
Below are 2 images of numbers, along with their graphs of predicted labels. 

1. ![Screen Shot 2021-07-07 at 10 04 24 PM](https://user-images.githubusercontent.com/60228369/125008117-cbab0680-e02f-11eb-9dff-4fb30ce430f0.png)

2. ![Screen Shot 2021-07-07 at 10 04 47 PM](https://user-images.githubusercontent.com/60228369/125008118-cbab0680-e02f-11eb-9d2f-79777535aa1e.png)


## 7) 
The mnist dataset seems to be more accurate than the fashion dataset. I think this is because the numbers are simpler images, and therefore more discernable to the software, and easier to sort into classes.
