# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages
### Step2:
Create the text using cv2.putText
### Step3:
Create the structuring element
### Step4:
Erode the image
## Program:

``` Python
# Import the necessary packages

import io
import os
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText

img = np.zeros((100,400), dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img,"REVERIE!",(5,70),font,2,(255,255,255),5,cv2.LINE_AA)

# Create the structuring element

kernel = np.ones((5,5), np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image


img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode, cmap = 'gray')
plt.axis("off")

# Dilate the image


img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate, cmap = 'gray')
plt.axis("off")



```
## Output:

### Display the input Image
![326513817-eec5606d-bdb5-42c8-ab02-027ec9399141](https://github.com/Vaishnavi-saravanan/erosion--dilation/assets/118541897/42bceab0-64ad-4b5d-badc-80b77b6ae46d)


### Display the Eroded Image

![326513970-06085f42-74e2-4bb0-849a-b02929d84149](https://github.com/Vaishnavi-saravanan/erosion--dilation/assets/118541897/7214b7e4-3d44-4470-93fb-33a1f44c23e9)

### Display the Dilated Image
![326514002-218aee74-33bc-4c43-985c-511ccded7b0e](https://github.com/Vaishnavi-saravanan/erosion--dilation/assets/118541897/0c26ced1-2b18-4a9a-91bd-d1607fc9d2a8)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
