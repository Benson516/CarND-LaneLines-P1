# **Finding Lane Lines on the Road** 


---

# Overview

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

# Reflection

## 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps:
- Morphological Openration on Color Image
- Low-pass filtering and Canny
- Selecting ROI
- Applying Hough-line Algorithm 
- Blending line on image

**1. Morphological Openration on Color Image**
Using morphological opening on original color image and get the local average of the intensity/color. Then substract the original color image by this local average to generate the local differences. This resulted in removal of effect by lightening/shadow and difference in road color (which occured in challenge.mp4)

**2. Low-pass filtering and Canny**
Low-pass filtering using Gaussian-blur and then apply canny.

**3. Selecting ROI**
Sellecting ROI to remove the region such as sky

**4. Applying Hough-line Algorithm**
Applying Hough-line algorithm for finding line segments, as well as drawing lines onto a blank image 

**5. Blending line on image**
Blending the original image with the line-image as final result





In order to draw a single line on the left and right lanes, I rewrite the draw_lines() function as draw_lines_thick_2() function. In draw_lines_thick_2() function, 

I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


## 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


## 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
