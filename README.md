# The Pixel-Based Adaptive Segmenter

## Description:
This approach follows a nonparametric background modeling paradigm. Thus, the background is modeled by a history of recently observed pixel values. The foreground decision depends on a decision threshold. The background update is based on a learning parameter.

Foreground segmentation is one of moving object detection techniques of computer vision applications. To date, modern moving object detection methods require complex background modeling and thresholds tuning to confront illumination changes. This method is an adaptive approach based on non-overlapping block texture representation. It aims to design a computationally light and efficient solution to improve the robustness of detection.

In this project, I provide a simple implementation of PBAS algorithm using python, also, I used an open-source implementation of c++ of this algorithm adding some post-processing modules and mask outputs.

### Requirements:
* opencv-3.0
* python-3.5
* numpy


### Algorithm steps:			
1. Read a Video <br />
2. Apply gaussian Filter <br />
3. Split each frame into 3 channels <br />
4. Initilize the model with zeros or using a simple background substraction algorithm <br />
5. Excute algorithm for each channel in parallel <br />
6. Apply bitwise_or between 3 outputs or bitwise_and between 3 outputs <br />
7. repeat until end of this video <br />


## Architecture of my project:
<pre>
- PBAS <br />
    |-- PBAS-C++ <br />
    |     |-- FeatureTracker.h <br />
    |     |-- FeatureTracker.cpp <br />
    |     |-- PBAS.h <br />
    |     |-- PBAS.cpp <br />
    |     |-- main.cpp <br />
    |-- PBAS-Python <br />
    |     | <br />
    |     |-- PBAS.py <br />
    | <br />
</pre>
