## Ex no: 10
## Date: 25/5/2022
# <p align="center">Implementation of Erosion and Dilation
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
Erode and Dilate the image.

### Step5:
End Program.

## Program:
```
DEVELOPED BY : VEERAMALAI S

REG NO : 212220230056
```

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
img1=np.zeros((200,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the Text using cv2.putText
cv2.putText(img1,' VEERA ',(5,70),font,2,(255),5,cv2.LINE_AA)
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
![Screenshot 2022-05-31 111007](https://user-images.githubusercontent.com/75234790/171101081-87042dfc-67c9-421e-bfe2-317c242b8d7c.png)


### Display the Eroded Image
![Screenshot 2022-05-31 111021](https://user-images.githubusercontent.com/75234790/171101088-4ed852e5-f065-46c7-919a-e9741a765e17.png)


### Display the Dilated Image

![Screenshot 2022-05-31 111035](https://user-images.githubusercontent.com/75234790/171101093-e4561876-cb97-4255-a6a6-4378c778d008.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
