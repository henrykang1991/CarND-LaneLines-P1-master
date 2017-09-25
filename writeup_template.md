# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 steps:

1. read image and convert the image into grey image;
2. conduct Gussian Smoothing on the grey image;
3. conduct Canny Edge Detection;
4. creat a polygon mask to define the ROI;
5. conduct Hough Transform line detection ;
6. delect the improper detected lines, connect the line segments and conduct line extrapolation. Initially, I got several lines which are not lane lines, so I extrapolated the lines and used the locations of the lines as a filter.


### 2. Identify potential shortcomings with your current pipeline

The pipeline works fine for the images and two videos with simpler conditions except that I have 2 lines for each side. For the challenge.mp4 video, my code did not work well due to the shadows of trees, unclear lane lines and uneven road surface. 


### 3. Suggest possible improvements to your pipeline

A possible improvement for the current code would be to use a line that lies in betwwen the two parallel lines for each lane line to represent lane line. For the lane line detect in the challege.mp4, advanced algorithm would be applied. 
