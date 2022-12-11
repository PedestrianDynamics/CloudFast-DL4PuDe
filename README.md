# **CloudFast-DL4PuDe:** A Cloud-based Deep Learning System for Improving Crowd Safety at Event Entrances
<p align="center">
<img src="./files/characterstcs2.png"/>
</p>

---

 [![License](https://img.shields.io/badge/License-BSD_3--Clause-blue.svg)](./LICENSE)  ![Python 3.7 | 3.8](https://img.shields.io/badge/Python-3.7|3.8-blue.svg)  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/abualia4/CloudFast-DL4PuDe/blob/main/CFSystem.ipynb)

This repisitory is for the following work
```
Ahmed Alia, ---  "A cloud-based deep learning system for improving crowd safety at event entrances", 2022
```

### Goal 
The system aims to early detect pushing patches automatically in running and crowded event entrances,  particularly in the live camera stream of entries.
### Motivation
 The motivation of the system is to help the organizers to make timely decisions before hazardous accidents develop and ensure smoother flows at entrances with higher levels of comfort and safety.
 
## Table of Contents
<ul>
<li>  <a href="#arch">The Architicture of CloudFast-DL4PuDe system </a>
<li><a href="#use">How to use CloudFast-DL4PuDe system</a>
<li> <a href="#demo">Demo</a>
<li> <a href="#CNN">Building and training the CNN architectures</a>
 <li><a href="#models">Trained CNN models</a>
<li><a href="#videos">Video experiments</a>
<li><a href="#time">Computational time evaluation</a>


### The Architicture of **CloudFast-DL4PuDe** System
<a name="arch"/>
<p align='center'>
<img src="./files/architicture.png" width='75%'>
</p>

**Notes**
1. This <a href="https://github.com/princeton-vl/RAFT">RAFT repository</a> is used for optical flow estimation in our system.
2. Some of <a href="https://colab.research.google.com/drive/1QnC7lV7oVFk5OZCm75fqbLAfD9qBy9bw">this notebook </a> is used for live streaming in our system.


### How to Use **CloudFast-DL4PuDe** System
<a name="use"/>

1. Click on  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/abualia4/CloudFast-DL4PuDe/blob/main/CFSystem.ipynb)
2. File--> save a copy in drive.
3. Download the cloud-fast-system directory.
4. Upload the cloud-fast-system directory to Google Colab at the same location of the copy of CFSystem.ipynp.

   ```     
    --Colab NoteBooks
         --copy of CFSystem.ipynp
         --cloud-fast-system
     ```    
5. For the input stream, we recommend using a virtual camera with one of the video recordings of crowded event entrances.
Video experiments are available in the video directory.
Kinly note that <a href="https://obsproject.com/">OBS studio</a> is free and open source software for virtual camera and live streaming.
6. Run copy of CFSystem.ipynp
---

### Demo
<a name="demo"/>

**Client side**
1. How to run
    * Launch the virtual camera based on the <a href="./videos/entrance2-undistorted-960-540.mp4">entrance2 video experiment</a> and OBS studio software.
    * Open the Jupyter Notebook (copy of CFSystem.ipynp) and entering the required inputs.
        -   patch=[2,4]
        -   roi=[107,55,669,270]
2. Video of the live camera stream with annotations of the predicted pushing patches,  red boxes represent the predicted patches.

<img src='./files/sample1.gif' />

3. Video of the live camera stream with annotations of the predicted pushing patches and ground truths, red circles refer to ground truths, while the red boxes represent the predicted patches.

 <img src='./files/sample2.gif'  />

---
### CNN Models
#### Building and Training the CNN Architectures
<a name="CNN"/>

1. Clone the repository in your directory.
```
git clone https://github.com/abualia4/CloudFast-DL4PuDe.git
```
2. Install the required libraries.
TensorFlow is the main required library
```
pip install tensorflow
```
3. Open this <a href="training-and-building-CNN-models/%20buildingAndTrainingCNNArchitectures.ipynb">notebook</a> and follow the guides.


#### Trained CNN Models
<a name="models"/>
The trained CNN models are available in the links below.
1. <a href="https://drive.google.com/drive/folders/1AHGJt4EQS3yWWKiihL8pE8QUUZZUdUim?usp=sharing"> Trained models in related work</a>.
2. <a href="https://drive.google.com/drive/folders/1p9NyGnij4tFhZWvscpP6KnCgcuhHV0eK?usp=share_link"> Trained popular CNN models</a>.


#### Dataset
<a name="dataset"/>
The dataset generated and used during this work are available from the corresponding authors upon request.
 ---
 

### Video Experiments
<a name="videos"/>
The original video experiments that were used in this work are available through the <a href="http://ped.fz-juelich.de/da">Pedestrian Dynamics Data Archive </a> hosted by the Forschungszentrum Juelich. Moreover, the undistorted videos are available through this <a href="./videos"/>link</a>.


### Computational Time Evaluation
<a name="time"/>
The results of the computational time evaluation of our and the baseline systems for each video experiment are available <a href="./computational-time">here</a>.

### Citataion
Will be added soon.

