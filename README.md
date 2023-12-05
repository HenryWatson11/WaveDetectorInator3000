# WaveDetectorInator3000
by Tucker Corwen and Henry Watson


Wave Classifier with Satellite Images
Welcome to the Wave Classifier repository! This project leverages state-of-the-art deep learning techniques to classify ocean waves using satellite images. Understanding and categorizing wave patterns in satellite imagery is a first step to being able to find new surf spots around the world.  

Overview:
Satellite imagery provides a unique perspective on Earth's oceans, offering a wealth of information about wave dynamics. This project employs a powerful convolutional neural network, specifically the InceptionV3 architecture for feature collection. We then trained a Logistic Regression on the feature collection from InceptionV3. In the end, our model was unsuccessful at accurately classifying images.

<img width="504" alt="Screen Shot 2023-12-05 at 1 43 33 AM" src="https://github.com/HenryWatson11/WaveDetectorInator3000/assets/152929762/a1b372d3-2b75-4894-b8a6-3e07fe430623">
Above is our test results boasting a measly 48% accuracy


Dataset:
To collect data we used the Google Earth Engine, a pruduct of goolge that allows for cloud computed exploration of the vast collection of satellite imagery. In specific we chose to use sentinel2 images because they gave us a high resolution of 10 meter pixels at a fairly high frequency of one image every 5-10 days. There were two main chalenges we encountered during data collection, cloud coverage and labeling.
Sadly, coastlines are often some of the cloudiest places in the world which made it hard for us to collect a large enough dataset from individual surf spots. Filtering out all images with more than 0% cloud coverage left us with a pretty small dataset. 5 years of satellite images of Biarritz, a popular surf spot in France yielded just 45 cloudless images. Image labeling was done all by hand which proved to be a very time consuming and tedious job. This fourther limited the size of our dataset given the time constraintes of our project.

<img width="401" alt="Screen Shot 2023-12-05 at 1 24 57 AM" src="https://github.com/HenryWatson11/WaveDetectorInator3000/assets/152929762/d545251a-c636-437a-bfc3-4287b2074c11">

Above is Biarritz on December 19 2021, Labeld as 2-4 feet

Due to to the limited size of our Dataset the distribution of wave size made for an unfavorable training set. 
<img width="400" alt="Screen Shot 2023-12-05 at 1 36 14 AM" src="https://github.com/HenryWatson11/WaveDetectorInator3000/assets/152929762/e32f5ed9-be2d-4b01-a615-b2bec9cde2c2">

This resulted in our model overfitting to the 2-4 feet result as seen in our confusion matrix below.
![confusion_matrix (1)](https://github.com/HenryWatson11/WaveDetectorInator3000/assets/152929762/97f03ce9-3a34-466e-9e61-6adec2586393)


Image Preprocessing: Prior to model training, satellite images undergo meticulous preprocessing, including resizing, normalization, and data augmentation. Fourthermore we flip each image inorder to double the size our dataset.
<img width="700" alt="Screen Shot 2023-12-05 at 11 00 33 AM" src="https://github.com/HenryWatson11/WaveDetectorInator3000/assets/152929762/3742fbd0-ca97-4560-9b1a-31ee6b96a3cf">

Key Takeaways:
Throughout this project Tucker and I never really felt comfortable with where we were at. Using Google Earth Engine proved to be difficult from the start as it's a platform neither of us had ever used before. Furthermore we were both new to java script as well as how images were stored. It took us a long time to finally get a collection of images downloaded and we still needed to label them by hand. All in all, data collection was quite the eye opening experience as to why deep learning models can be so challenging to train. After all, our model failed to beat fifty percent accuracy due to a shortage of data. 
In the code attatched you will se many of our unused snippets.




