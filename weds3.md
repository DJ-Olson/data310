# Wealth Class Dataset

## Import the dataset city_persons.csv to your PyCharm environment
I ended up using Jupyter Notebook since pycharm was giving me some issues. To import the data into Jupyter Notebook I simply copied the data link and then downloaded a csv file to my desktop. I then used pandas to create a dataframe.


## Initially set the target to the least wealthy class, 2 in this case, and set all other wealth class outcomes to 0 (3,4 & 5)
This step was simple. The only thing that had to be changed from the provided script was setting the target value equal to 1. 


## Train, validate and test your model
Training the model required the column names to be changed. This dataset was not too hard to work with because the variables were numeric. I used bucketized columns (every 10 years) for age and indicator columns for the rest of the variables. 


## Interpret and analyze your results. Did the model performance exhibit a particular trend?
![Screen Shot 2021-07-21 at 9 41 21 PM](https://user-images.githubusercontent.com/60228369/126652999-b562b7df-19fc-4488-80b7-72b4d0585aec.png)
![Screen Shot 2021-07-21 at 9 41 37 PM](https://user-images.githubusercontent.com/60228369/126653004-a289cf1f-5e84-4bb2-aa81-49025b12649c.png)

The two images above show the results for setting all the wealth classes equal to the target. As you can see, wealth class 2 was very accurate, and wealth class 3 did well. Then the data got far less accurate for wealth classes 4 and 5. 
