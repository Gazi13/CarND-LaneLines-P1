

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

[//]: # (Image References)

[image1]: ./examples/laneLines_thirdPass.jpg "img1"
[image2]: ./examples/line-segments-example.jpg "img2"
My pipeline consisted of 5 steps.
1. Convert image to grayscale
2. Apply gaussian blue to grayscale image
3. Apply canny edge detection to blured image
4. Extract the region of interest area from edged image
5. Find the lines by using "Hough Line Transform"

In order to draw a single line on the left and right lanes, we need to modified the draw_lines() function. After hough transform we have too mant lines. We need to convert this lines to a single line. To do this
1. Classify the lines (Left and right) according their slope.
2. Find average slope and bias.
3. Calculate the x and y coordinates of the line.


![alt text][image1]  ![alt text][image2]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
