# Image Convolutions

## Question 1
#### In this exercise you manually applied a 3x3 array as a filter to an image of two people ascending an outdoor staircase. Modify the existing filter and if needed the associated weight in order to apply your new filters to the image 3 times. Plot each result, upload them to your response, and describe how each filter transformed the existing image as it convolved through the original array and reduced the object size. What are you functionally accomplishing as you apply the filter to your original array? Why is the application of a convolving filter to an image useful for computer vision? Stretch goal: instead of using the misc.ascent() image from scipy, can you apply three filters and weights to your own selected image? Describe your results.

![Screen Shot 2021-07-15 at 10 26 33 AM](https://user-images.githubusercontent.com/60228369/125806181-827bfee4-c83c-4706-8374-39bdb65ed611.png)
![Screen Shot 2021-07-15 at 10 26 50 AM](https://user-images.githubusercontent.com/60228369/125806179-aebd6bad-2958-4185-9d2a-1c6c9a91bc71.png)
![Screen Shot 2021-07-15 at 10 27 07 AM](https://user-images.githubusercontent.com/60228369/125806177-8541a2a8-c967-4153-bd72-d5f5d6031d94.png)


#
Above are the 3 images I convolved. I ran this filter: [ [-1, 1, 1], [0, 0, -1], [-2, 1, 1]] 3 times, but multipled all the numbers in it by 10 with each consecutive run. It seems like as the filters ran, the larger filters enhanced the emphasis on both the horizontal and vertical lines. This makes sense because what an image filter does is go over an image by scanning each pixel and examining the neighboring pixels. It then multiplies these pixel values by the weights given in the filter. So, larger values would naturally provide stronger highlights to the similarities (such as vertical and horizontal lines) within an image. 


## Question 2
#### Another useful method is pooling. Apply a 2x2 filter to one of your convolved images, and plot the result. In effect what have you accomplished by applying this filter? Does there seem to be a logic (i.e. maximizing, averaging or minimizing values?) associated with the pooling filter provided in the example exercise (convolutions & pooling)? Did the resulting image increase in size or decrease? Why would this method be useful? Stretch goal: again, instead of using misc.ascent(), apply the pooling filter to one of your transformed images.

![Screen Shot 2021-07-16 at 12 31 04 PM](https://user-images.githubusercontent.com/60228369/125979805-4b34e5d9-6a93-4f42-acd2-44de78b8c36e.png)

#
I applied the pooling method to the last image from the previous question. By using the pooling method we are able to maintain the important features of the image while making it smaller by combining pixels. This is done by pooling pixels and keeping the ones that are largest. By doing this the image size decreased. This method would be useful for compressing images while keeping important features. This would help avoid softwares getting slowed down by lots of large images. 


##
#### Below is the resulting matrix from convolving the 3x3 filter over the 9x9 matrix.

![Screen Shot 2021-07-16 at 7 50 37 PM](https://user-images.githubusercontent.com/60228369/126018566-132eb4e4-a6d8-43f4-b73e-5238dec7eaf9.png)



