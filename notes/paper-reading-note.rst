.. note:: This is a review of papers under the subject of driving fatigue and computer vision.

Efficient Car Alarming System for Fatigue Detection during Driving (2012)
=========================================================================

Abstract
--------

The algorithm work in three stages:

1. the face of the driver is detected and tracked.
2. the facial features are extracted for further processing.
3. eye's status is monitored.

---------------------------------------

.. figure:: images/paper1.png
    :scale: 42 %
    :alt: image


- **Face detection** is done by using Viola and Jones algorithm.
- **Eye deetection** is done by using edge detection. "Canny Edge detector", "Sobel Edge detector"
- **Eye Status detection**, intensity change, for example, in eyebrow, upper edge and lower edge of eye.


An Improved Fatigue Detection System Based on Behavioral Characteristics of Driver (2017)
=========================================================================================

Signs / Symptoms of Drowsyness
-------------------------------

- Blinking frequently and partially closed eyes
- Not able to remember the traveled path
- Yawning after every small period
- Drifting or move out from the lane
- Head nodding
- Poor concentration
- Slow reactions

.. note:: This paper will focus on the features related to eye and mouth like frequent blinking and yawning etc. 

Idea
----

After getting the face image, it sends to Support Vector Machine (SVM) classifier which classifies the facial image as fatigued or not.

Proposed System
---------------

- Video Capture Unit
- Face Detection Unit and Features Extraction
- Fatigue Detection on Extracted Features

---------------------------------------

.. figure:: images/paper2.png
    :scale: 25 %
    :alt: image
    :align: left


A System of Driving Fatigue Detection Based on Machine Vision and Its Application on Smart Device (2014)
=========================================================================================================

Abstract
--------

*keywords: machine vision, Adaboost algorithm (face and eye classifier)*

The method is implemented on smart phones or tablets.

The approach has four steps:
- image preprocessing (denoising)
- face detection
- eye state recognition
- fatigue evaluation

---------------------------------------

.. figure:: images/paper3-scr.png
    :scale: 50 %
    :alt: image
    :align: left



Improved Detection Strategy
---------------------------

Front face classifier, left / right-deflected face classifier. 

*For example*, when the system misses the target using the front face classifier, right deflected face classifier is called firstly to re-detect. If it succeeds, the right deflected face classifier will be used in the next frame. 


Fatigue Judgement
-----------------

**PERCLOS** is Percentage of Duration of Closed-Eye State in a specific time interval (1 min or 30 s).

It is a well-recognized and effective measure of neurophysiological fatigue level. In this system, only two eye states: open and closed can be detected.

---------------------------------------

.. figure:: images/paper3.png


Hybrid Computer Vision System for Drivers' Eye Recognition and Fatigue Monitoring (2014)
========================================================================================


Abstract
--------

The setup consists of two cameras operating in the visible and near infra-red-spectra, respectively.

.. note:: not very applicable for our project which only uses a web-cam. Maybe later.


Eye Blink Detection
===================


Traditional Methods for Computing Blinks
----------------------------------------

1. Eye localization.
2. Thresholding to find the whites of the eyes.
3. Determining if the "white" region of the eyes disappears for a period of time (indicating a blink).

The Noval, Fancy Detection Method
---------------------------------

The detection is built upon computing a metric called **eye aspect ratio (EAR)**.

.. figure:: images/blink1.jpeg
    :scale: 50 %
    :alt: image
    :align: left
    
.. figure:: images/blink2.jpeg
    :scale: 50 %
    :alt: image
    :align: left
    
.. figure:: images/blink3.png
    :scale: 20 %
    :alt: image
    :align: left

