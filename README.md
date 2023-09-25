# The concept of HLoc in brief

## HLoc : Hierarchical Localization - A toolbox for visual localisation
It is the process of estimating the position or orientation (pose) of a robot or sensor within a larger environment.

HLoc allows robots and autonomous systems to have a robust and scalable approach to understanding their position and orientation in complex and dynamic environments.

## Table of Contents
* [Steps for HLoc](#hloc-steps)
* [SuperGlue](#superglue)
* [SuperPoint](#superpoint)
* [Structure-from-Motion(SfM)](#SfM)
* [Image Matching](#image-matching)
* [SLAM](#slam)
* [Camera Calibration](#camera-calibration)
* [Image Registration](#image-registration)
* [Detectors-Descriptors](#detectors-descriptors)
* [R2D2](#r2d2)
* [6-DoF](#6dof)
* [Image Stiching](#image-stiching)
* [Feature Extraction and Matching](#feature-extraction-matching)

## Steps for performing HLoc
The following are the steps for performing HLoc :


### Datasets

Prepare the datasets and make sure to upload them if the datasets are present locally in Google Colab.
Organize the dataset into a directory structure compatible with the HLoc framework.
Ensure that the dataset contains images and any metadata required for localization and mapping.

If the dataset is not already available locally, you can use the provided code to download and unzip the dataset. In your code, this is done using the following lines :
```
if not images.exists():
    !wget http://path.zip -P datasets/
    !unzip -q datasets/name.zip -d datasets/
```  
  

  
### Feature Extraction and Matching

Extract distinctive visual features from each image in the dataset. 
Common feature types include keypoints and descriptors.

Then perform feature matching between pairs of images to find correspondences between keypoints or descriptors.

Configure your variables for feature extraction and matching.
You can choose different feature extraction and matching methods from the available configurations or create your own if needed.


### Pose Estimation

Estimate the relative pose between the pairs of images of the matched features.

### Localisation
### Visualisation


## SuperGlue

SuperGlue is an algorithm used as a graph neural network for feature matching.
It is a CV algorithm developed for matching and estimating the correspondences between images.


## SuperPoint

The algorithm's primary goal is to detect distinctive features or keypoints of images and provide corresponding descriptors that can be used for various CV tasks.


## Structure-from-Motion(SfM)

It is a Computer Vision and Photogrammatic technique used for the reconstruction of the 3D structure of a given scene from a set of 2D images or video frames.


## Image Matching

The goal of image mapping is to identify regions, features or objects in one image that correspond to region, feature or object in another image.


## SLAM

It refers to the ability of a robot or a device to simultaneously create a map of its environment and determine it's own position within that enivronment in real-time while it moves and observes the surroundings.


## Camera Calibration

The main goal of camera calibration is to correct any irregularities or distortions made by the camera module or sensor for accurate measurements.
It basically determines the intrinsic and extrinsic parameters of a camera to model its imaging characteristics accurately.


#### Intrinsic Properties : 
* Focal Length(fx, fy) -> Convergence and Divergence
* Principal Point(cx, cy) -> Optical Center
* Distortion Coefficients(k1, k2, p1, p2, k3) -> This includes lens distortion, radial and tangential distortions making straight lines appear curved.

#### Extrinsic Properties :  
* Rotation Matrix(R) -> It is the camera's orientation and specifies how the camera is rotated in 3D space.
* Translation Vector(T) -> The camera's position in 3D space.

#### Image Size : 
* Width and Height

#### Camera Model :
* The type of camera used to capture the images, like a pinhole or fisheye camera

#### Calibration Error Metrics : 
* It determines the quality of calibration, like reprojection error or root mean square error, indicating how well the calibrated camera parameters fit the observed image data.

## Image Registration

Image registration refers to the process of aligning two or more images of the same scene or object to a common coordinate system, such that corresponding features or keypoints in the images overlap or match as closely as possible.


## Detectors-Descriptors


### Detectors : 
They are algorithms or methods used to identify key points or points of interest in an image.
These keypoints are the features of the image, which include edges, corners, or blobs.

The primary purpose of detectors is to locate regions in an image that are likely to contain important visual information.
Detectors output a list of key points or feature points, each characterized by its location (coordinates) within the image.

Examples : 
* Harris Corner Detector
* Shi-Tomasi Corner Detector
* FAST(Features from Accelerated Segment Test)
* SIFT(Scale-Invariant Feature Transform)
* SURF(Speeded-Up Robust Features)

### Descriptors :
They are algorithms or methods used to characterize the visual appearance of key points detected in the image. 
They capture information about the local image region surrounding each key point.

The primary purpose of descriptors is to create numerical representations (feature vectors) of key points that are distinctive and invariant to various transformations such as rotation, illumination and changes in scale.

They output feature vectors that encode information about the local image content around each key point. 
These vectors are designed to be robust to changes in viewpoint and lighting conditions.

Examples : 
* SIFT
* SURF
* BRIEF(Binary Robust Independent Elementary Features)
* ORB(Oriented FAST and Rotated BRIEF)
* FREAK(Fast Retina Key point)


##### After detecting key points and computing descriptors for multiple images, feature matching is performed to find correspondences between key points in different images.
##### This is usually done using distance metrics like Euclidean distance (or) Hamming distance for binary descriptors.

##### In summary, detectors identify key points in images while descriptors provide numerical representations of those key points. Together, they enable the extraction of the distinctive and robust features from images, which are crucial for various Computer Vision tasks .


## R2D2 - Reliable and Repeatable Detector and Descriptor



## 6-DoF
## Image Stiching
## Feature Extraction and Matching
