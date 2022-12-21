# Fundamental-Matrix-Calculation
Computer Vision Calculation of Fundamental Matrix using 8 point algorithm

## Introduction
Implementing calculation of fundamental matrix using 8 point algorithm which is an algorithm used in computer vision to estimate the essential matrix or the fundamental matrix related to a stereo camera pair from a set of corresponding image points.

## Dataset
The dataset is the kusvod2 dataset. Image files are of the form <something>A.png and <something>B.png for each image pair.

## Tasks
1. Find keypoints and correspondences between two images
2. Implement the 8 point algorithm
* shift and scale
* compute design matrix
* perform SVD to find null space
* compute draft fundamental matrix
* Perform an SVD of the draft fundamental matrix, set the smallest singular value to zero and reassemble so that F now has determinant = 0
* Calculate which correspondences are inliers and which are outliers using this F
* Wrap previous steps in a RANSAC loop that runs enough times that you have a probability > 99% of finding 8 inliers and computing a good quality F
* Re-estimate F using all the inliers
* Compute F in terms of the original pixel coordinate
3. Randomly sample 10 keypoint pairs from correspondences detected as inliers, display these on the images together with epipolar lines

## Result
<img width="807" alt="image" src="https://user-images.githubusercontent.com/88305416/208819524-a52c9270-30b8-4bfb-9ac2-ac6cf195ff2f.png">

Score 6/7
