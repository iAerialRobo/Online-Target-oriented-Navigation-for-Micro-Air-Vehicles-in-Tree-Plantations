# ForaNav: Insect-inspired Online Target-oriented Navigation for MAVs in Tree Plantations

<p align="center">
<img src="https://github.com/user-attachments/assets/95a3672b-d25e-49cd-b3b5-21e49b9d5b76" width="600" style="display: block; margin: 0 auto">


## Overview
ForaNav is an insect-inspired, online target-oriented navigation system designed for Micro Air Vehicles (MAVs) operating in tree plantations. The system integrates real-time tree detection with bio-inspired navigation strategies to enable efficient and autonomous UAV flight in cluttered environments.

This repository contains two main components:

[Tree detection](https://github.com/iAerialRobo/Online-Target-oriented-Navigation-for-Micro-Air-Vehicles-in-Tree-Plantations/tree/59a8627617de2e210af7e12cd6dd247c16fb667e/Tree_Detection): 
To achieve real-time oil palm tree detection on resource-restricted MAVs, we use HOG features and an SVM classifier. Our method further improves detection by distinguishing oil palm trees from similar palm species and background objects with star-shaped features.

[Navigation](https://github.com/iAerialRobo/Online-Target-oriented-Navigation-for-Micro-Air-Vehicles-in-Tree-Plantations/tree/283f0fe028a0f36eaa476db4d197dd84313a3b4b/Navigation): 
Our navigation strategy draws inspiration from insect foraging behavior, particularly the reliance on local visual cues and their body-centered frame of reference for position estimation and efficient movement.

## Citation
If you use this code in an academic context, please cite our work:
````
Weijie Kuang, Hann Woei Ho, Ye Zhou and Shahrel Azmin Suandi, ForaNav: Insect-inspired Online Target-oriented Navigation for MAVs in Tree Plantations.
(The code will be released upon publication.)
````

## Tree detection
The [Tree detection](https://github.com/iAerialRobo/Online-Target-oriented-Navigation-for-Micro-Air-Vehicles-in-Tree-Plantations/tree/59a8627617de2e210af7e12cd6dd247c16fb667e/Tree_Detection) folder contains the implementation of the proposed tree detection approach. It includes:

- [SVM Training Code](https://github.com/iAerialRobo/Online-Target-oriented-Navigation-for-Micro-Air-Vehicles-in-Tree-Plantations/blob/157d1ccc2b9007e685d0078fdb9c8dfb7c5179d6/Tree_Detection/SVM_train.py): Scripts for training the proposed Histogram of Oriented Gradients (HOG)-based SVM model.
- [Lightweight Deep Learning Training Code](https://github.com/iAerialRobo/Online-Target-oriented-Navigation-for-Micro-Air-Vehicles-in-Tree-Plantations/blob/157d1ccc2b9007e685d0078fdb9c8dfb7c5179d6/Tree_Detection/Lightweight_DL_model_training.py): Implementation of deep learning-based tree detection for comparison, including MobileNetV2 and EfficientNet.
- [Pre-trained SVM Model](https://github.com/iAerialRobo/Online-Target-oriented-Navigation-for-Micro-Air-Vehicles-in-Tree-Plantations/blob/157d1ccc2b9007e685d0078fdb9c8dfb7c5179d6/Tree_Detection/SVM_model.joblib): The trained SVM model for oil palm tree detection.
- [HOG-based Detection Algorithm](https://github.com/iAerialRobo/Online-Target-oriented-Navigation-for-Micro-Air-Vehicles-in-Tree-Plantations/blob/157d1ccc2b9007e685d0078fdb9c8dfb7c5179d6/Tree_Detection/HOG_based_detecion.py): The proposed tree detection method using the trained SVM model.
- [Oil Palm Tree Dataset](https://drive.google.com/file/d/1pqzwsjBEopTnlbHHbPO2hpJrrhZ_qyu1/view?usp=sharing): The dataset used for training and evaluating the models.

<p align="center">
<img src="https://github.com/user-attachments/assets/c7cd4b89-a56c-4901-b9dc-4d2f73aea6dc" width="400" style="display: block; margin: 0 auto">
p>
  
## Hardware Configuration
The MAV platform used in this research consists of the following components:

- Crazyflie Bolt Flight Controller
  
- JeVois A33 Machine Vision Camera
  
- Loco Positioning Deck
  
- Flow Deck V2
  
![prototype of the detection](https://github.com/user-attachments/assets/aa7be72e-c6d4-4641-a871-e3c967e81afe)
