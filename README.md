# WaveDetectorInator3000
by Tucker Corwen and Henry Watson


Wave Classifier with Satellite Images
Welcome to the Wave Classifier repository! This project leverages state-of-the-art deep learning techniques to classify ocean waves using satellite images. Understanding and categorizing wave patterns in satellite imagery is a first step to being able to find new surf spots around the world.  

Overview
Satellite imagery provides a unique perspective on Earth's oceans, offering a wealth of information about wave dynamics. This project employs a powerful convolutional neural network, specifically the InceptionV3 architecture for feature collection.

Dataset
To collect data we used the Google Earth Engine, a pruduct of goolge that allows for cloud computed exploration of the vast collection of satellite imagery. In specific we chose to use sentinel2 images because they gave us a high resolution of 10 meter pixels at a fairly high frequency of one image every 5-10 days. There were two main chalenges we encountered during data collection, cloud coverage and labeling.
Sadly, coastlines are often some of the cloudiest places in the world which made it hard for us to collect a large enough dataset from individual surf spots. Filtering out images with cloud coverage of 

Image Preprocessing: Prior to model training, satellite images undergo meticulous preprocessing, including resizing, normalization, and data augmentation. Fourthermore we flip each image inorder to double the size our dataset.

