# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the necessary modules.

### Step2
For performing smoothing operation on a image.

Average filter
```
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
```
Weighted average filter
```
wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
```
Gaussian Blur
```
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
```
Median filter
```
median_blur=cv2.medianBlur(image,11)
```
### Step3
For performing sharpening on a image.

Laplacian Kernel
```
lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
lap_image=cv2.filter2D(image,-1,lap_kernel)
```
Laplacian Operator
```
Lap_sharp=cv2.Laplacian(image,cv2.CV_64F)
```
### Step4
Display all the images with their respective filters.

## Program:
### Developed By   :Sanjay P
### Register Number:212220230042


### 1. Smoothing Filters
### i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("Eat.jpeg")
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
### ii) Using Weighted Averaging Filter
```
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
### iii) Using Gaussian Filter
```
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

### iv) Using Median Filter
```
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
### i) Using Laplacian Kernal
```
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
### ii) Using Laplacian Operator
```
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
</br>

i) Using Averaging Filter

![1](https://user-images.githubusercontent.com/75235426/174441635-00c37197-2ba1-4f72-9787-44199a81d2f0.jpg)

ii) Using Weighted Averaging Filter

![2](https://user-images.githubusercontent.com/75235426/174441641-dee037d3-bbcf-4ab7-96ac-1e6786b5cb9f.jpg)

iii) Using Gaussian Filter

![3](https://user-images.githubusercontent.com/75235426/174441651-7ef80496-ad7b-48d8-8b2d-bc84c154b384.jpg)

iv) Using Median Filter

![4](https://user-images.githubusercontent.com/75235426/174441655-b7c1df29-95d9-428d-b713-a3dfbc6e3137.jpg)

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

![5](https://user-images.githubusercontent.com/75235426/174441662-d6e8fdb4-908d-4c89-a9fe-bc3e29d9248c.jpg)

ii) Using Laplacian Operator

![6](https://user-images.githubusercontent.com/75235426/174441665-a61bfcca-028a-4e1a-8a68-7e9f20f052fa.jpg)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
