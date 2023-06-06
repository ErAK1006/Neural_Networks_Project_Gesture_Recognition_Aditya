# Neural_Networks_Project_Gesture_Recognition
Imagine you are working as a data scientist at a home electronics company which manufactures state of the art smart televisions. You want to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.

## Table of Contents
* General Info
* Technologies Used
* Conclusions
* Acknowledgements


## General Information
Imagine you are working as a data scientist at a home electronics company which manufactures state of the art smart televisions. You want to develop a cool feature in the smart-TV that can recognise five different gestures performed by the user which will help users control the TV without using a remote.

The gestures are continuously monitored by the webcam mounted on the TV. Each gesture corresponds to a specific command:

* Thumbs up: Increase the volume
* Thumbs down: Decrease the volume
* Left swipe: 'Jump' backwards 10 seconds
* Right swipe: 'Jump' forward 10 seconds
* Stop: Pause the movie

Each video is a sequence of 30 frames (or images)

## Conclusions
The conv2D network will extract a feature vector for each image, and a sequence of these feature vectors is then fed to an RNN-based network. The output of the RNN is a regular softmax (for a classification problem such as this one).

There are a few key things to note about the Conv-RNN architecture:

* You can use transfer learning in the 2D CNN layer rather than training your own CNN
* GRU can be a better choice than an LSTM since it has lesser number of gates (and thus parameters)

#### 3D Convolutional Network, or Conv3D
3D convolutions are a natural extension to the 2D convolutions you are already familiar with. Just like in 2D conv, you move the filter in two directions (x and y), in 3D conv, you move the filter in three directions (x, y and z). In this case, the input to a 3D conv is a video (which is a sequence of 30 RGB images). If we assume that the shape of each image is 100x100x3, for example, the video becomes a 4-D tensor of shape 100x100x3x30 which can be written as (100x100x30)x3 where 3 is the number of channels. Hence, deriving the analogy from 2-D convolutions where a 2-D kernel/filter (a square filter) is represented as (fxf)xc where f is filter size and c is the number of channels, a 3-D kernel/filter (a 'cubic' filter) is represented as (fxfxf)xc (here c = 3 since the input images have three channels). This cubic filter will now '3D-convolve' on each of the three channels of the (100x100x30) tensor.

## Technologies Used
* Visual Studio Code (Version: 1.78.2)

## Acknowledgements
Give credit here.
* References by Upgrad

## Team
* Aditya Kumar Pal
* Ganesh Babu

## Contact
Created by [@ErAK1006]

https://github.com/ErAK1006/Neural_Networks_Project_Gesture_Recognition_Aditya
