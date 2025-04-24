# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1
Import the required libraries.

## Step2
Convert the image from BGR to RGB.

## Step3
Apply the required filters for the image separately.

## Step4
Plot the original and filtered image by using matplotlib.pyplot.>


## Program:
### Developed By : Sabeeha Shaik
### Register Number: 212223230176
</br>

### 1. Smoothing Filters

## i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("coffee.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()



```
## ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
## iii) Using Gaussian Filter
```

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()



```
## iv)Using Median Filter
```


median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()


```

## 2. Sharpening Filters
## i) Using Laplacian Linear Kernel
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()




```
## ii) Using Laplacian Operator
```

laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()



```

## OUTPUT:
## 1. Smoothing Filters

### i) Using Averaging Filter
![image](https://github.com/user-attachments/assets/5b6bfba9-8958-4456-b9a1-822a4d49a3e2)


### ii)Using Weighted Averaging Filter
![image](https://github.com/user-attachments/assets/31448cd6-a802-41ea-8782-e2a3084641f7)


### iii)Using Gaussian Filter
![image](https://github.com/user-attachments/assets/29cd1631-7ce6-4bf8-8d40-77ed55f315b4)


### iv) Using Median Filter
![image](https://github.com/user-attachments/assets/67ec1ec2-7e19-407c-a4be-67b72ded1903)


## 2. Sharpening Filters


### i) Using Laplacian Kernel
![image](https://github.com/user-attachments/assets/dc6279ea-b699-4648-addb-da08b8073a61)


### ii) Using Laplacian Operator
![image](https://github.com/user-attachments/assets/702d8a4f-fdec-423c-8439-ea0a7360c020)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
