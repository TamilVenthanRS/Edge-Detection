# Edge-Detection
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.
### Step2:
For performing edge detection on a image.
Sobel
```
sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(img,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(img,cv2.CV_64F,1,1,5)
```
Laplacian
```
Laplacian=cv2.Laplacian(img,cv2.CV_64F)
Canny
canny=cv2.Canny(img,120,150)
```

### Step3:
Display all the images with their respective edge detected images.

## Program:

``` Python
# Import the packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1=cv2.imread ('coco.jpg') 
gray_image = cv2.cvtColor(image1,cv2.COLOR_BGR2GRAY)
plt.title('GRAY IMAGE')
plt.imshow(gray_image,cmap = 'gray')
img = cv2.GaussianBlur(gray,(3,3),0)
sobelx = cv2.Sobel(gray_image,cv2.CV_64F,1,0,ksize=5)
sobely = cv2.Sobel(gray_image,cv2.CV_64F,0,1,ksize=5)
sobelxy =cv2.Sobel(gray_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(1)
plt.subplot(2,2,1)
plt.imshow(gray_image,cmap = 'gray')
plt.title('Original'), plt.xticks([]), plt.yticks([])
plt.subplot(2,2,2)
plt.imshow(sobelx,cmap='gray')
plt.title('sobelx')
plt.xticks([]), plt.yticks([])
plt.subplot(2,2,3)
plt.imshow(sobely,cmap='gray')
plt.title('sobely')
plt.xticks([]), plt.yticks([])
plt.subplot(2,2,4)
plt.imshow(sobelxy,cmap='gray')
plt.title('sobelxy')
plt.xticks([]), plt.yticks([])
plt.show()
# LAPLACIAN EDGE DETECTOR
laplacian = cv2.Laplacian(gray_image,cv2.CV_64F)
plt.imshow(laplacian,cmap='gray')
plt.title('laplacian')
plt.show()
# CANNY EDGE DETECTOR
canny_edges = cv2.Canny(gray_image, 120, 150)
plt.imshow(canny_edges,cmap='gray')
plt.title('canny_edges')
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
<br>

![2022-05-18](https://user-images.githubusercontent.com/75235477/169008785-7d81c47d-34ec-4973-bba4-1eeefa0e5509.png)
<br>


### LAPLACIAN EDGE DETECTOR
<br>

![7-2](https://user-images.githubusercontent.com/75235477/169008460-fac082bf-12c0-4f2a-a594-5574bd3f31de.png)
<br>


### CANNY EDGE DETECTOR
<br>

![7-3](https://user-images.githubusercontent.com/75235477/169008480-6961873f-a932-4ca7-bad8-b744426adeb0.png)
<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
