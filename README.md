# WaveDetectorInator3000
by Tucker Corwen and Henry Watson


Wave Classifier with Satellite Images
Welcome to the Wave Classifier repository! This project leverages state-of-the-art deep learning techniques to classify ocean waves using satellite images. Understanding and categorizing wave patterns in satellite imagery is a first step to being able to find new surf spots around the world.  

Overview
Satellite imagery provides a unique perspective on Earth's oceans, offering a wealth of information about wave dynamics. This project employs a powerful convolutional neural network, specifically the InceptionV3 architecture for feature collection.

Dataset
To collect data we used the Google Earth Engine, a pruduct of goolge that allows for cloud computed exploration of the vast collection of satellite imagery. In specific we chose to use sentinel2 images because they gave us a high resolution of 10 meter pixels at a fairly high frequency of one image every 5-10 days. There were two main chalenges we encountered during data collection, cloud coverage and labeling.
Sadly, coastlines are often some of the cloudiest places in the world which made it hard for us to collect a large enough dataset from individual surf spots. Filtering out all images with more than 0% cloud coverage left us with a pretty small dataset. 5 years of satellite images of Biarritz, a popular surf spot in France yielded just 45 cloudless images. Image labeling was done all by hand which proved to be a very time consuming and tedious job. This fourther limited the size of our dataset given the time constraintes of our project.

<img width="401" alt="Screen Shot 2023-12-05 at 1 24 57 AM" src="https://github.com/HenryWatson11/WaveDetectorInator3000/assets/152929762/d545251a-c636-437a-bfc3-4287b2074c11">

Above is Biarritz on December 19 2021, Labeld as 2-4 feet

Due to to limited size of our Dataset the distribution of wave size made for an unfavorable training set. 
<img width="400" alt="Screen Shot 2023-12-05 at 1 36 14 AM" src="https://github.com/HenryWatson11/WaveDetectorInator3000/assets/152929762/e32f5ed9-be2d-4b01-a615-b2bec9cde2c2">

Image Preprocessing: Prior to model training, satellite images undergo meticulous preprocessing, including resizing, normalization, and data augmentation. Fourthermore we flip each image inorder to double the size our dataset.

Key Takeaways



