# corrosion
estimating corrosion using image processing and SVM or n-layered NN


Basically, I am using the property of Entropy variation with contrast to find a corroded area or patch on a metal surface because CNN is not good enough for classification of corrosion. We though of using the property of Natural vs Artificial texture and pass it through a svm or any n-layered neural network. 

The First Image is corroded and is imported as image1

![old](https://user-images.githubusercontent.com/27013287/62388194-4c2a7800-b57a-11e9-932d-b3826d97329e.jpg)


The non Corroded Image is 

![new](https://user-images.githubusercontent.com/27013287/62390693-80089c00-b580-11e9-826d-3b3963acef22.jpg)


Properties of each pixels is studied on the basis of change in entropy with respect to contrast. By finding GLCM and taking Greycoprops, the texture data is carried as the Grey Level Co Occurance Matrix which keeps a track how many times two numbers have appeared together

on the third image when we pic a certain pixel with the cursor it goes into the svm and predict if it will corroded or non corroded. Even if has been done for one image. The average rate of could be used for training in the svm for multiple images and then tested on multiple images. 

image3

![image1](https://user-images.githubusercontent.com/27013287/62392090-2904c600-b584-11e9-84c1-e161a0117f1e.jpg)


