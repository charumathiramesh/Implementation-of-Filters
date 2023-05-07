# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import cv2, matplotlib.py libraries and read the saved images using cv2.imread().

### Step2
Convert the saved BGR image to RGB using cvtColor(). 

### Step3
By using the following filters for image smoothing:filter2D(src, ddepth, kernel), Box filter,Weighted Average filter,GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType]]]), medianBlur(src, ksize),and for image sharpening:Laplacian Kernel,Laplacian Operator.

### Step4
Apply the filters using cv2.filter2D() for each respective filters.

### Step5
Plot the images of the original one and the filtered one using plt.figure() and cv2.imshow().

## Program:
### Developed By   : charumathi R
### Register Number: 212222240021


### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("image.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
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
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()





```

iv) Using Median Filter
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
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
ii) Using Laplacian Operator
```Python

laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
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
### 1. Smoothing Filters


i) Using Averaging Filter

![230782922-7bbef89e-7775-4c2a-83da-6ac0971ae167](https://user-images.githubusercontent.com/120204455/236689946-34602816-3de3-4f54-8c8a-fa9231d2976a.png)



ii) Using Weighted Averaging Filter
![230782931-28355ef8-7b24-4937-8c65-d85995641aac](https://user-images.githubusercontent.com/120204455/236689733-40d41ec2-2f9d-41e5-8600-2085607cb0a9.png)


iii) Using Gaussian Filters
![230782940-cd9c341d-b937-49be-9361-0f00c4dbd70a](https://user-images.githubusercontent.com/120204455/236689746-1fb4227a-d0f8-47e5-aa5f-f55d9984e83d.png)


iv) Using Median Filter

![230782952-0c5f93dc-5b98-42e5-bd27-8cca69955c85](https://user-images.githubusercontent.com/120204455/236689753-b7e32e2c-a3cf-4ca4-8c0e-ea5cf27407cc.png)


### 2. Sharpening Filters


i) Using Laplacian Kernal


![230782966-5dcae3f5-caf6-4cfb-bbc4-41ec47a44bbb](https://user-images.githubusercontent.com/120204455/236689763-ca54af0c-8b63-40dc-b46b-e15846dd2402.png)

ii) Using Laplacian Operator

![230782979-10368a13-1698-4a0a-80a0-3881df391de3](https://user-images.githubusercontent.com/120204455/236689768-b3b773a0-3885-4f06-8e46-4dd255abb4ab.png)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
