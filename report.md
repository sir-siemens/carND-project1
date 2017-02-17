#**Finding Lane Lines on the Road** 

##Writeup Template

###You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

###1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 8 steps. 

#### convert to gray scale 
#### gaussian blur
#### canny edge detection
#### extract region of interest based on 8 vertices
#### find lines using hough transformation
#### classify lines to either left or right line or unrelevant  
#### least square line regression (organize all the points for representing lines into two arrays and find the best fit for left lane and right lane )
#### extrapolation (compute the intersection between the best fit line and ROI ) 

I didn't modify draw_lines funtions since my result only contains two lines

 


###2. Identify potential shortcomings with your current pipeline

If no lines are found in the image,  line regression would not work. This is the case for the optional challenge. Wrong edge detection at the shadow or the rand of the highway may influence the result. 


###3. Suggest possible improvements to your pipeline

A possible improvement would be to synthetic a list of points for each line segment and use RANSAC to fit the points.

 
