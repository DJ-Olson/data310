# Part 1
Part 1 includes multi-class linear regression and a multi-class DNN regression using the provided target and features. The target was 'highway-mpg' and the features were: 'num-of-cylinders', 'engine-size', 'horsepower', and 'curb-weight.'

## Linear loss model and prediction plot
![Screen Shot 2021-07-12 at 10 17 18 PM](https://user-images.githubusercontent.com/60228369/125385889-5b6eee80-e369-11eb-94ec-65e41c148e3b.png)
![Screen Shot 2021-07-12 at 10 21 08 PM](https://user-images.githubusercontent.com/60228369/125385887-5b6eee80-e369-11eb-92ad-79b92b804859.png)
## DNN loss model and prediction plot
![Screen Shot 2021-07-12 at 10 19 01 PM](https://user-images.githubusercontent.com/60228369/125385893-6033a280-e369-11eb-97eb-165145ceec8f.png)
![Screen Shot 2021-07-12 at 10 20 58 PM](https://user-images.githubusercontent.com/60228369/125385894-6033a280-e369-11eb-8953-4e27ccbe4b51.png)
## Mean Absolute Error Table
### (Ignore horsepower models)
![Screen Shot 2021-07-12 at 10 07 12 PM](https://user-images.githubusercontent.com/60228369/125385896-60cc3900-e369-11eb-9511-0bf5f17fe79f.png)
## 
Upon examining the graphs and the absolute error table, it seems apparent that the linear regression model performed better than the DNN regression model.


# Part 2
For the second part of the project I added new features to try to improve the models. The target stayed the same (highway-mpg), and all the old features remained, but I also added the features 'city-mpg', 'engine-type', and 'normalized-loss'.


## Linear loss model and prediction plot
![Screen Shot 2021-07-12 at 11 20 07 PM](https://user-images.githubusercontent.com/60228369/125386314-0f707980-e36a-11eb-9f15-f368984fa611.png)
![Screen Shot 2021-07-12 at 11 22 11 PM](https://user-images.githubusercontent.com/60228369/125386318-10a1a680-e36a-11eb-9665-39b690cccf97.png)
## DNN loss model and prediction plot
![Screen Shot 2021-07-12 at 11 20 55 PM](https://user-images.githubusercontent.com/60228369/125386320-113a3d00-e36a-11eb-8f0b-c5137ab0109a.png)
![Screen Shot 2021-07-12 at 11 23 00 PM](https://user-images.githubusercontent.com/60228369/125386322-126b6a00-e36a-11eb-8da3-34b7363e7d84.png)
## Mean Absolute Error Table
### (Ignore horsepower models)
![Screen Shot 2021-07-12 at 11 21 19 PM](https://user-images.githubusercontent.com/60228369/125386324-14352d80-e36a-11eb-9f6c-b2db505e553e.png)

## 
After adding these new features both the Linear and DNN regression models improved. I am most impressed with the drastic improvement of the linear model. The prediction plot looks very good with almost all the points falling very close to the line, and the error table shows a significant decrease from 2.3 to just above 1. 
