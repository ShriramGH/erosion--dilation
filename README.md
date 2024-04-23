# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Insert the text using cv2.putText()
- Step3: The perform the erosion for given text and display the text using imshow()
- Step4: Next,perform dilation for inout text and display the result
## Program:
```
DEVELOPED BY: SHRIRAM s
REGISTER NUMBER: 212222240098
```
### Import the necessary packages
```python
import cv2
import numpy as np 
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```python
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Shriram',(5,70),font,2,(255),5,cv2.LINE_AA)
```
### Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
### Erode the image
```python
image_erode1=cv2.erode(img1,kernel1)
plt.imshow(image_erode1)
plt.axis("off")
```
### Dilate the image
```python
image_dilate1=cv2.dilate(img1,kernel1)
plt.imshow(image_dilate1)
plt.axis("off")
```
## Output:
### Display the input Image

![image](https://github.com/ShriramGH/erosion--dilation/assets/117991122/ad4ac1fd-2ea3-4d83-acec-84a09bc53682)

### Display the Eroded Image

![image](https://github.com/ShriramGH/erosion--dilation/assets/117991122/ee2dc288-24d0-4455-b0bf-ab738ad0da9b)

### Display the Dilated Image

![image](https://github.com/ShriramGH/erosion--dilation/assets/117991122/872b016c-0c04-4fcf-82b8-50a69af4b09e)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
