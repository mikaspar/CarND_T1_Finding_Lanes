# Project 1 Finding Lanes
## Overview
Python code written in Jupyter Notebook for finding lane lines in a an image and video made with a dash-cam.
## Includes
* Finding_Lane_Lines_KA for JPG image
  * ipynb file - source code for Jupyter Notebook
  * test.jpg - test image
* Finding_Lanes_Lines_Video_KA for MP4 video
  * ipynb file - source code for Jupyter Notebook
  * test_outpu_KA.mp4 - video result
## Algorithm
1. read image
2. convert image into gray scale
3. filter out pepper and salt
4. find Canny edges
5. define the region of interest
6. apply Hough transform for edges in region of interest
7. extrapolate detected edges to right and left lane lines ( 1st order polynoms)
8. write result
