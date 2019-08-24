# Corrosion
Estimating corrosion using image processing and SVM

This Text has two parts:
- The steps in the code
- The theory behind the code.

1. Steps in the code...


a) Import Libraries
b) Upload the pics of high entropy less entropy and one test image
c) Extract image data and save it
d) Data Frame formation by stacking up values
e) Entering non corroded data en
j) Entropy and contrast with prediction value
f) Signing values to X as entropy contrast and Y as outputs (0/1) 
g) Segregating points as corroded and non corroded only on the basis of output Y
h) Fit SVM in the data set
i) Getting the test image selecting one pixel and predicting its value for (0/1)
j) Use SVC.predict to get the value (0/1)
k) Get output in the form of corroded and non corroded

2. Theory Behind the Code:

Basically, I am using the property of Entropy variation with contrast to find a corroded area or patch on a metal surface because CNN is not good enough for classification of corrosion. We though of using the property of Natural vs Artificial texture and pass it through a svm or any n-layered neural network.

A Co-Occurence Matrix, also referred to as a co occurrence distribution is defined over an image to be the distribution of co-occurring values at a given offset, Represents the distance and angular spatial relationship over an image sub region of specific size. The GLCM calculates how often a pixel with grayscale intensity value i occurs either horizontally, vertically or diagonally to adjacent pixels with the value of i. 

![image](https://user-images.githubusercontent.com/27013287/62852151-3c432e80-bd06-11e9-95eb-1dba3fa6c923.png)





The First Image is corroded and is imported as image1

![old](https://user-images.githubusercontent.com/27013287/62388194-4c2a7800-b57a-11e9-932d-b3826d97329e.jpg)


The non Corroded Image is 


![new](https://user-images.githubusercontent.com/27013287/62390693-80089c00-b580-11e9-826d-3b3963acef22.jpg)


Properties of each pixels is studied on the basis of change in entropy with respect to contrast. By finding GLCM and taking Greycoprops, the texture data is carried as the Grey Level Co Occurance Matrix which keeps a track how many times two numbers have appeared together

on the third image when we pic a certain pixel with the cursor it goes into the svm and predict if it will corroded or non corroded. Even if has been done for one image. The average rate of could be used for training in the svm for multiple images and then tested on multiple images. 

image3


![image1](https://user-images.githubusercontent.com/27013287/62392090-2904c600-b584-11e9-84c1-e161a0117f1e.jpg)


This is the graph that we got


![image](https://user-images.githubusercontent.com/27013287/62846772-3f332480-bcf0-11e9-9a72-ac0744d24c21.png)



the file linked to it was performed only on one image but it gave tangible results so further work includes to perform it on thousands of image and see the results. 
