# Implementation-of-Erosion-and-Dilation

## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Erode the image using cv2.erode().

### Step5:
Dilate the image using cv2.dilate().

 
## Program:

```python

# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt
# Load the Image
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
# Create the Text using cv2.putText
cv2.putText(img1,'Ganesh',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,cmap='gray')
# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
# Erode the image
img_erode=cv2.erode(img1,kernel1)
plt.imshow(img_erode,cmap='gray')

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
plt.imshow(img_dilate,cmap='gray')


```
## Output:

### Display the input Image

![e10](https://user-images.githubusercontent.com/75235006/172300634-ac8fe47c-a5ed-49ed-8587-6d44ee3b5142.png)


### Display the Eroded Image

![e11](https://user-images.githubusercontent.com/75235006/172300648-f6d666ba-5f14-4ab9-b6df-449cd43f89be.png)


### Display the Dilated Image

![e12](https://user-images.githubusercontent.com/75235006/172300659-1a3b85dc-4a64-454a-849d-3c2efa5291e8.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
