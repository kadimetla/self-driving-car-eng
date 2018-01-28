# **Finding Lane Lines on the Road**



---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteCurve.jpg "Grayscale"
[image2]: ./test_images_output/solidYellowCurve.jpg "Grayscale"
[image3]: ./test_images_output/solidWhiteRight.jpg "Grayscale"
[image4]: ./test_images_output/whiteCarLaneSwitch.jpg "Grayscale"
[image5]: ./test_images_output/solidYellowLeft.jpg "Grayscale"


---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps.
1. Convert image to gray scale image.
2. Guassian filter to blur image.
3. Canny algorithm to detect edges in image.
4. Region of interest mask.
5. Hough Transform to find lane lines.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by separating line segments by their slope as left and right line. Negative slope as left line and Positive slope as right line.
Computed slope and intercept for each point left and right line points.
Computed mean slope and intercept of left and right line points.
Computed x1 and x2 points using y - mean(intercepts ) / mean(slopes)  for both left and right line.

If you'd like to include images to show how the pipeline works, here is how to include an image:

![solidWhiteCurve.jpg][image1]
![solidYellowCurve.jpg][image2]
![solidWhiteRight.jpg][image3]
![whiteCarLaneSwitch.jpg][image4]
![solidYellowLeft.jpg][image5]



### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when road does not have white lanes.

Another shortcoming could be night driving.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to improvement to region of interest.

Another potential improvement could be to  draw_lines.
