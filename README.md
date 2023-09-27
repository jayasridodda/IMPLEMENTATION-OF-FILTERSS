# IMPLEMENTATION-OF-FILTERS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.

### Step2
Convert the image from BGR to RGB.

### Step3
Apply the required filters for the image separately.

### Step4
Plot the original and filtered image by using matplotlib.pyplot

### Step5
End the program.


## Program:
#### Developed By   : JAYASRI DODDA
#### Register Number: 212222240028
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("ex6.jpeg")
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
ii) Using Weighted Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("ex6.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
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
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("ex6.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
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
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("ex6.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
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

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("ex6.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
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
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("ex6.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
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
![Screenshot from 2023-09-27 11-13-18](https://github.com/jayasridodda/IMPLEMENTATION-OF-FILTERSS/assets/123259278/5b8dd709-1b08-4873-b41e-88074bbdab01)



ii) Using Weighted Averaging Filter
![Screenshot from 2023-09-27 11-13-56](https://github.com/jayasridodda/IMPLEMENTATION-OF-FILTERSS/assets/123259278/722f9357-60bb-44e1-ba5f-2a966e517530)


iii) Using Gaussian Filter
![Screenshot from 2023-09-27 11-14-27](https://github.com/jayasridodda/IMPLEMENTATION-OF-FILTERSS/assets/123259278/5ddd7bef-3efa-4599-9e7d-c4db721525f2)


iv) Using Median Filter
![Screenshot from 2023-09-27 11-15-05](https://github.com/jayasridodda/IMPLEMENTATION-OF-FILTERSS/assets/123259278/aa447907-3252-459b-9d39-80e506e65231)


### 2. Sharpening Filters

i) Using Laplacian Kernal
![Screenshot from 2023-09-27 11-15-31](https://github.com/jayasridodda/IMPLEMENTATION-OF-FILTERSS/assets/123259278/8d6f47c1-bc5c-4528-b988-7973857df8f0)

ii) Using Laplacian Operator
![Screenshot from 2023-09-27 11-16-40](https://github.com/jayasridodda/IMPLEMENTATION-OF-FILTERSS/assets/123259278/787946c4-7b29-43f8-afc5-41a0592e434f)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
