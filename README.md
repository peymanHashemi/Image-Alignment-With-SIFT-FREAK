# Image Alignment With SIFT & FREAK

This project focuses on image alignment and feature descriptor performance evaluation. The tasks involve using different descriptors to match and align a rotated image back to its original orientation. The primary objective is to analyze the robustness of these descriptors under image transformations such as rotation.

# Content
- Table of Contents
  * [Task 1: Image Alignment Using SIFT](#Task-1-Image-Alignment-Using-SIFT) 
  * [Task 2: Descriptor Comparison Using FREAK](#Task-2-Descriptor-Comparison-Using-FREAK)  
  * [METHOD Task 1](#Task-1)
  * [METHOD Task 2](#Task-2)
 
## Task 1: Image Alignment Using SIFT
In the first task, you will:

* Select a random image and apply a random rotation to it.
* Extract features from the original image using the SIFT (Scale-Invariant Feature Transform) descriptor.
* Match these features with the rotated image and use the matched points to compute a transformation matrix.
* Align the rotated image back to its original orientation using methods such as affine or perspective transformations.
* Visualize the matched key points between the original and rotated images and repeat the process for two different random rotations.

## Task 2: Descriptor Comparison Using FREAK

In the second task, you will:

* Repeat the alignment process from Task 1 but use the FREAK (Fast Retina Keypoint) descriptor instead of SIFT.
* Compare SIFT and FREAK in terms of performance, speed, and accuracy.
* Analyze which descriptor is more resistant to rotation and document your findings.

# METHOD

## Task 1:

* Image Rotation:

The input image is rotated by a random angle using OpenCV’s warpAffine. Padding is added to avoid cropping.

* Grayscale Conversion:

Both the original and rotated images are converted to grayscale for feature extraction.

* Feature Extraction and Matching:

SIFT (Scale-Invariant Feature Transform) is used to detect and describe keypoints in both images.
The detected keypoints are matched using a Brute-Force Matcher with a ratio test to filter good matches.

* Homography Estimation and Image Warping:

A homography matrix is calculated using the matched keypoints.
The rotated image is warped back to its original orientation using warpPerspective.

* Visualization:
* 
Keypoints and matches are visualized, along with the final aligned image.

### Results of SIFT:

<img style="width:700px" src="https://github.com/user-attachments/assets/975420b0-280f-4e4a-b9b1-8d8807c34ba3"> <br>
<img style="width:400px" src="https://github.com/user-attachments/assets/1df0c8d3-2c82-4be0-9517-0a624752b2e3">
<img style="width:300px" src="https://github.com/user-attachments/assets/7b01ecca-f606-401e-a9d3-2d3cb789fcc6"><br>
<img style="width:800px" src="https://github.com/user-attachments/assets/e3f4a13c-f75d-4c0f-880e-943d2179dd25"><br>
<img style="width:800px" src="https://github.com/user-attachments/assets/fe62b772-a0c6-4b37-8481-7a93205fab16">

### For step-by-step results, check the [SIFT]https://github.com/peymanHashemi/Image-Alignment-With-SIFT-and-FREAK/blob/3275f2b70cc22a0a535b2ac5ba8f90ad379e15dd/SIFT.ipynb).


## Task 2: 

* Image Rotation and Preprocessing:

Similar to Task 1, the image is rotated and converted to grayscale.

* Feature Extraction and Matching:

FREAK (Fast Retina Keypoint) descriptors are computed after detecting keypoints using either SIFT or FAST.
Keypoints are matched using a Hamming-based Brute-Force Matcher.

* Homography and Image Warping:

The same process is followed to estimate the homography and warp the rotated image back to its original position.

* Comparison and Analysis:

The performance of SIFT and FREAK is compared in terms of:

* Speed: FREAK is faster due to its binary descriptor format.
* Accuracy and Robustness: SIFT generally performs better for precise alignment, but FREAK’s efficiency makes it ideal for real-time applications.
### Results of FREAK:

<img style="width:700px" src="https://github.com/user-attachments/assets/70776e44-a3f3-44da-8aae-498c75165c6f"><br>
<img style="width:350px" src="https://github.com/user-attachments/assets/051323a9-06c0-4064-90e6-d105e931930c">
<img style="width:350px" src="https://github.com/user-attachments/assets/46e9c467-992b-45c1-bcc4-fb1fae81e3e6"><br>
<img style="width:800px" src="https://github.com/user-attachments/assets/4485ed1b-a13d-4670-92b3-56630a55d8df"><br>
<img style="width:800px" src="https://github.com/user-attachments/assets/95d4926b-7a64-4cce-8383-b5be87c9f038">

### For step-by-step results, check the [FREAK](https://github.com/peymanHashemi/Image-Alignment-With-SIFT-FREAK/blob/46304ec6632cb577b6b5090a98133893e72854cb/FREAK.ipynb).
