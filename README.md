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
### Datasets

Prepare your datasets and make sure to have upload them if the datasets are present locally in Google Colab.
Organize your dataset into a directory structure compatible with the HLoc framework.
Ensure that your dataset contains images and any metadata required for localization and mapping.

If your dataset is not already available locally, you can use the provided code to download and unzip your dataset. In your code, this is done using the following lines:
```
if not images.exists():
    !wget http://path.zip -P datasets/
    !unzip -q datasets/name.zip -d datasets/
```  
  

  
### Feature Extraction and Matching

Configure your variables for feature extraction and matching.
You can choose different feature extraction and matching methods from the available configurations or create your own if needed.


### Pose Estimation

### Localisation
### Visualisation
* 
## SuperGlue
## SuperPoint
## Structure-from-Motion(SfM)
## Image Matching
## SLAM
## Camera Calibration
## Image Registration
## Detectors-Descriptors
## R2D2
## 6-DoF
## Image Stiching
## Feature Extraction and Matching

The following are the steps for performing HLoc 

