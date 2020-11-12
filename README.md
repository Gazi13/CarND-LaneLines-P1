

### Reflection

### Pipeline Describtion

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

Before
![alt text][image2] 
After 
![alt text][image1]  

