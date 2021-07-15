# Image Convolutions

## Part 1
### In this exercise you manually applied a 3x3 array as a filter to an image of two people ascending an outdoor staircase. Modify the existing filter and if needed the associated weight in order to apply your new filters to the image 3 times. Plot each result, upload them to your response, and describe how each filter transformed the existing image as it convolved through the original array and reduced the object size. What are you functionally accomplishing as you apply the filter to your original array? Why is the application of a convolving filter to an image useful for computer vision? Stretch goal: instead of using the misc.ascent() image from scipy, can you apply three filters and weights to your own selected image? Describe your results.

![Screen Shot 2021-07-15 at 10 26 33 AM](https://user-images.githubusercontent.com/60228369/125806181-827bfee4-c83c-4706-8374-39bdb65ed611.png)
![Screen Shot 2021-07-15 at 10 26 50 AM](https://user-images.githubusercontent.com/60228369/125806179-aebd6bad-2958-4185-9d2a-1c6c9a91bc71.png)
![Screen Shot 2021-07-15 at 10 27 07 AM](https://user-images.githubusercontent.com/60228369/125806177-8541a2a8-c967-4153-bd72-d5f5d6031d94.png)


#
Above are the 3 images I convolved. I ran this filter: [ [-1, 1, 1], [0, 0, -1], [-2, 1, 1]] 3 times, but multipled all the numbers in it by 10 with each consecutive run. It seems like as the filters ran, the larger filters enhanced the emphasis on both the horizontal and vertical lines. This makes sense because what an image filter does is go over an image by scanning each pixel and examining the neighboring pixels. It then multiplies these pixel values by the weights given in the filter. So, larger values would naturally provide stronger highlights to the similarities (such as vertical and horizontal lines) within an image. 
