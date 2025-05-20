# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Create a blank image.

### Step2:
Create a structuring element (5x5 rectangular)

### Step3:
Erode the image.

### Step4:
Dilate the image.

### Step5:
End the program.

 
## Program:

```
# Developed By: JAGADEESH P
# Register No: 212223230083


import cv2
import numpy as np
from matplotlib import pyplot as plt
# Load the image
img1=np.zeros((100,700),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL

# Create the text using cv2.putText
cv2.putText(img1,'jaga' ,(5,70),font,4,(255),2,cv2.LINE_AA)


# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))

# Dilate the image
img_dilate=cv2.dilate(img1,kernel1)
img_erode=cv2.erode(img1,kernel1)

# Display the results
plt.figure(figsize=(12, 5))
plt.subplot(1,3,1)
plt.imshow(img1,cmap='gray')
plt.subplot(1,3,2)
plt.imshow(img_dilate,cmap='gray')
plt.subplot(1,3,3)
plt.imshow(img_erode,cmap='gray')


```
## Output:

### Display the input Image:
![WhatsApp Image 2025-05-20 at 22 09 05_1f05d8aa](https://github.com/user-attachments/assets/5ef2929b-d62c-418a-abef-5deef192194b)


### Display the Eroded Image:
![WhatsApp Image 2025-05-20 at 22 09 06_fe3fd7d5](https://github.com/user-attachments/assets/03cb4ebc-6a6a-4571-b77d-7dc9ca819a35)

### Display the Dilated Image:
![WhatsApp Image 2025-05-20 at 22 09 05_325bc3c4](https://github.com/user-attachments/assets/db9c3757-9cb0-4af3-b00f-bc2a1e32e8bc)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
