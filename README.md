# The concept of HLoc in brief

## HLoc : Hierarchical Localization - A toolbox for visual Localization
It is the process of estimating the position or orientation (pose) of a robot or sensor within a large environment.

HLoc allows robots and autonomous systems to have a robust and scalable approach to understanding their position and orientation in complex and dynamic environments.

Following are the key topics to get familiar with to work with HLoc.

## Table of Contents
* [Steps for performing HLoc](#hloc-steps)
* [SuperPoint](#superpoint)
* [SuperGlue](#superglue)
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



## SuperPoint

The algorithm's primary goal is to detect distinctive features or keypoints of images and provide corresponding descriptors that can be used for various CV tasks particularly if you are working on image feature extraction and matching.


SuperPoint is built upon the Convolution Neural Network (CNN) architecture.


Some of the important features of SuperPoint are :
* SuperPoint has the ability to detect the key points in an image automatically.
* It also generates the description of features from the extracted key points.
* SuperPoint is self-supervised, i.e., it does not require manual supervision while generating key points or descriptors during training. It is trained on unlabeled image data.
* It is designed to efficiently run on GPU and is suitable for real-time applications.



## SuperGlue

SuperGlue is an algorithm used as a graph neural network for feature matching.
It is a CV algorithm developed for matching and estimating the correspondences between images.
It was introduced as an extension to the SuperPoint model.

Some of the important features of SuperGlue are :
* Used as feature matching to find correlations between key points or feature points in different images.
* It uses the Geometric Verification step, where it ensures that the matched features are not just similar but also consistent with the expected geometric relationships between the images.
* SuperGlue is built upon Graph Neural Networks (GNN)


## Structure-from-Motion(SfM)

It is a Computer Vision and Photogrammatic technique used for the reconstruction of the 3D structure of a given scene from a set of 2D images or video frames.




## Image Matching

The goal of image mapping is to identify regions, features, or objects in one image that correspond to a region, feature, or object in another image.




## SLAM

It refers to the ability of a robot or a device to simultaneously create a map of its environment and determine it's own position within that environment in real-time while it moves and observes the surroundings.




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


##### After detecting key points and computing descriptors for multiple images, feature matching is performed to find correspondences between key points in different images. This is usually done using distance metrics like Euclidean distance (or) Hamming distance for binary descriptors.

##### In summary, detectors identify key points in images while descriptors provide numerical representations of those key points. Together, they enable the extraction of the distinctive and robust features from images, which are crucial for various Computer Vision tasks .




## R2D2 - Reliable and Repeatable Detector and Descriptor

R2D2 aims to predict a set of sparse locations of an image I, that are repeatable and reliable for the purpose of local feature matching.




## 6-DoF

Six-degree-of-freedom localisation refers to the process of determining the precise position and orientation of an object or sensor in 3D space along six-different axes or degrees of freedom.

* Translation along the X - axis
* Translation along the Y - axis
* Translation along the Z - axis
* Rotation about the X - axis
* Rotation about the Y - axis
* Rotation about the Z - axis

-> 6-DoF enables precise tracking and positioning of objects or devices in 3D space.

-> Accurate 6-DoF localisation requires the use of specialized sensors and algorithms such as inertial measurement units(IMUs), GPS, Lidar, cameras and depth sensors.

-> The goal is to provide precise and real-time information about an object's or device's position and orientation in 3D space.




## Image Stiching

Image stitching is a Computer Vision technique that combines multiple overlapping images into a single, larger and seamless panaramic image.

The process of image stitching involves aligning, blending, and merging individual images to create a unified and continuous view of a scene that extends beyond the field of view of a single image.




## Feature Extraction and Matching
"Extractors" and "Matchers" are key components used for feature-based image analysis. 
These are essential for identifying and matching distinctive features or key points between images.

### Feature Extraction : 
* An algorithm used to detect and describe distinctive local features or key points in an image.
* It's main goal is to find characteristic points of interest in an image that can be used for matching, recognition and more.
* Examples : SIFT, SURF, ORB and Harris Corner
  
### Feature Matching : 
* An algorithm used to compare and establish correspondences between features or key points detected in multiple images.
* It is crucial for tasks like image alignment, object tracking and image stitching. It helps identify common features in different images, allowing for estimation of transformations between them.
* Examples : Brute-Force Matcher, FLANN, and RANSAC  
