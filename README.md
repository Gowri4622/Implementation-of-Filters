# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the necessary modules.
</br>
</br> 

### Step2
For performing smoothing operation on a image.

* Average filter
```
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
```
* Weighted average filter
```
wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
```

* Gaussian Blur
```
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
```

* Median filter
```
median_blur=cv2.medianBlur(image,11)
```
</br>
</br> 

### Step3
For performing sharpening on a image.

* Laplacian Kernel
```
lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
lap_image=cv2.filter2D(image,-1,lap_kernel)
```

* Laplacian Operator
```
Lap_sharp=cv2.Laplacian(image,cv2.CV_64F)
```
</br>
</br> 

### Step4
Display all the images with their respective filters.
</br>
</br> 



## Program:
### Developed By   : Gowri M
### Register Number: 212220230019
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
average_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Average Filter image')
plt.imshow(average_filter_image)
plt.show()
```

ii) Using Weighted Averaging Filter
```Python
weight_average_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weight_average_filter_image=cv2.filter2D(image,-1,weight_average_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image[30:200,50:200])
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Weighted average Filter image')
plt.imshow(weight_average_filter_image[30:200,50:200])
plt.show()
```

iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Gaussian Filter image')
plt.imshow(gaussian_blur)
plt.show()
```

iv) Using Median Filter
```Python
median_blur=cv2.medianBlur(image,11)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Median Filter image')
plt.imshow(median_blur)
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
laplacian_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
laplacian_image=cv2.filter2D(image,-1,laplacian_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Kernel Filter image')
plt.imshow(laplacian_image)
plt.show()
```

ii) Using Laplacian Operator
```Python
Laplacian_sharp=cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Operator Filter image')
plt.imshow(Laplacian_sharp)
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
</br>
![Screenshot_628](https://user-images.githubusercontent.com/75235455/166292663-56adc236-d604-4284-9930-c9f03f575f95.png)
</br>
</br>
</br>

ii) Using Weighted Averaging Filter
![Screenshot_629](https://user-images.githubusercontent.com/75235455/166292690-937cd82e-f457-4161-8b75-0fa852db3ba0.png)
</br>
</br>
</br>
</br>
</br>

iii) Using Gaussian Filter
![Screenshot_630](https://user-images.githubusercontent.com/75235455/166292704-40c589aa-6777-4817-99b6-0ccbab0adb8b.png)
</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter
![Screenshot_631](https://user-images.githubusercontent.com/75235455/166292734-cc9ee083-8356-454c-b2d6-2a8554d542d9.png)
</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![Screenshot_632](https://user-images.githubusercontent.com/75235455/166292763-0171aff8-ba9f-4cfb-9b35-206fb04a2d6f.png)
</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
![Screenshot_633](https://user-images.githubusercontent.com/75235455/166292793-a4333195-75ba-4bed-aba5-f3b63fcf6772.png)
</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
