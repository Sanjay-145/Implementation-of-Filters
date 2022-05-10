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

i) Using Averaging Filter
```Python




```
ii) Using Weighted Averaging Filter
```Python





```
iii) Using Gaussian Filter
```Python





```

iv) Using Median Filter
```Python





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python





```
ii) Using Laplacian Operator
```Python





```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter
</br>
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter
</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter
</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
