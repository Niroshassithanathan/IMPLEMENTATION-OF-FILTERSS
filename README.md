# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1
Import cv2, matplotlib.py libraries and read the saved images using cv2.imread().

## Step2
Convert the saved BGR image to RGB using cvtColor().

## Step3
By using the following filters for image smoothing:filter2D(src, ddepth, kernel), Box filter,Weighted Average filter,GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType]]]), medianBlur(src, ksize),and for image sharpening:Laplacian Kernel,Laplacian Operator.

## Step4
Apply the filters using cv2.filter2D() for each respective filters.

## Step5
Plot the images of the original one and the filtered one using plt.figure() and cv2.imshow().

## Program:
### Developed By   :NIROSHA S
### Register Number:212222230097


### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("lion.jpg")
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
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lion.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Weighted Averaging Filter Image")
plt.axis("off")





```
iii) Using Gaussian Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lion.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Filter Image")
plt.axis("off")




```

iv) Using Median Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lion.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Filter Image")
plt.axis("off")





```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lion.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Laplacian kernelFiltered Image")
plt.axis("off")





```
ii) Using Laplacian Operator
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lion.jpg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title(" Laplacian operator Filtered Image")
plt.axis("off")





```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter
![Screenshot from 2023-09-13 15-06-01](https://github.com/Niroshassithanathan/IMPLEMENTATION-OF-FILTERSS/assets/121418437/ce553b44-6da4-4edf-9ffd-19dd8558fd50)


ii) Using Weighted Averaging Filter
![Screenshot from 2023-09-13 15-06-34](https://github.com/Niroshassithanathan/IMPLEMENTATION-OF-FILTERSS/assets/121418437/f9f46a0c-4849-4ce1-aae2-6df73c0c19e1)

iii) Using Gaussian Filter
![Screenshot from 2023-09-13 15-06-56](https://github.com/Niroshassithanathan/IMPLEMENTATION-OF-FILTERSS/assets/121418437/127625e1-f7ed-484c-b791-0e6061f6014d)

iv) Using Median Filter
![Screenshot from 2023-09-13 15-07-11](https://github.com/Niroshassithanathan/IMPLEMENTATION-OF-FILTERSS/assets/121418437/f145446e-993e-4417-8ea4-cc00dd571f35)

### 2. Sharpening Filters


i) Using Laplacian Kernal
![Screenshot from 2023-09-13 15-07-21](https://github.com/Niroshassithanathan/IMPLEMENTATION-OF-FILTERSS/assets/121418437/1167c1ea-6dce-4d8d-a446-2ef267033395)


ii) Using Laplacian Operator
![Screenshot from 2023-09-13 15-07-48](https://github.com/Niroshassithanathan/IMPLEMENTATION-OF-FILTERSS/assets/121418437/995ec932-461c-405f-996e-6ab87114d3a8)



## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
