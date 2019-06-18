# CAOS -  Continuous Angle Orientation System

Authors:
- Davide Brinati - d.brinati@campus.unimib.it
- Davide Meloni - d.meloni5@campus.unimib.it
- Alberto Raimondi - a.raimondi21@campus.unimib.it


<p align="center">
  <img width="200" height="200" src="https://github.com/done1892/Advanced-Machine-Learning-Project/blob/master/pics/logo.png">
</p>

# 

The task of image orientation consists in the prediction of the most
natural angle that a human would use to take a picture. In this paper
we propose CAOS, a new system to allow a common convolutional
neural network to deal with the cyclical nature of predicting the nat-
ural angle of an image. The solution is not straightforward due to
the periodic behavior of angles. The model proposed is a supervised
neural network that avoids the need to previously and feature points
or landmarks but uses a standard convolutional neural network with
a particular kind of loss function and output pair. The model reaches
state of the art results in a specific domain without signs of overftting

#

- The PDF file contains the report about this work.

* The dataset is available at this link:

  http://www.robots.ox.ac.uk/~vgg/data/vgg_face2/

- The ipynb file contains Pytorch implementation of CAOS, described below.

  The first part of the notebook includes initialization of functions which will be used in dataloader to perform geometric transformations, such as rotations, cropping, etc.
  After, a Pytorch dataloader has been instantiated, it can handle one channel images and performs preprocessing and data augumentation, and after that feeds the neural network.
  The pretrained NN used for this task is SqueezeNet which outputs an array of two elements. The network has been trained through stochastic gradient descending using the Adam Optimizer. The Loss function used is customized and compare the chord between the angle predicted by the network and its real value. Gradients optimize this function in the training loop for 80 epochs.
  In the last part the trained model has been used for inference, and evaluation on some images
  
  For further details please open PDF file, which contains the report on the work.
  
- Below the live demo of CAOS:

<p align="center">
  <img width="600" height="500" src="https://github.com/done1892/Advanced-Machine-Learning-Project/blob/master/pics/CAOS-Demo.gif">
</p>

 

  https://drive.google.com/open?id=1lhpo31ZOITBNggDLJiajHV0Pm-fKDuhd
  
