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

Prepare your datasets and make sure to upload them if the datasets are present locally in Google Colab.
Organize your dataset into a directory structure compatible with the HLoc framework.
Ensure that your dataset contains images and any metadata required for localization and mapping.

If your dataset is not already available locally, you can use the provided code to download and unzip your dataset. In your code, this is done using the following lines :
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
## Camera Calibration
## Image Registration
## Detectors-Descriptors
## R2D2
## 6-DoF
## Image Stiching
## Feature Extraction and Matching
