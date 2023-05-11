# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.
## Program:
### Developed by: Harsha vardhan
### Register no: 212222240114

### Import the necessary packages
``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt


```
### Create the Text using cv2.putText

``` Python
img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Harsha',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()
```
### Create the structuring element


``` Python
kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))
```
### Use Opening operation
``` Python
image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()


```
### Use Closing Operation
``` Python
image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()




```
## Output:

### Display the input Image
![OUTPUT](/11.1.png)


### Display the result of Opening
![OUTPUT](/11.2.png)

### Display the result of Closing
![OUTPUT](/11.3.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.