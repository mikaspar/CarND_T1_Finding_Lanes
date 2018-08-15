## Overview
Python code written in Jupyter Notebook for finding lane lines in a an image and video made with a dash-cam.

## Algorithm

My pipeline consits of following steps: 

1. read image
2. convert image into gray scale
3. filter out pepper and salt using Gauss
4. find Canny edges
5. define the region of interest
6. apply Hough transform for edges in region of interest
7. extrapolate detected edges to right and left lane lines ( 1st order polynoms)
8. write result

## Results

The designed pipeline works well, but it is a sufficient method for the easiest cases only. A deeper development of the pipeline is necessary for more general usage of this method. The pipeline was tested successfully on solidWhiteRight and solidYellowLeft videos. The results on the challenge video show shortcomings discussed in the next chapter.

## Shortcomings

* if the contrast between the road surface and the lane is not large engough, no lane line ist detected.
* for inter- and extrapolation of the lane lines was used 1st order polynomial, which is unsufficient in curves.
* fixed designed area of interest may result in detecting wrong edges.

## Possible improvements

* Improve the sensibility of the lane line detection on road surfaces with low contrast between line and road surface.
* Use polonymial of higher order for the inter-/extrapolation of lane lines.
* Design a dynamic area of interest, based on direction of the drive.

 
