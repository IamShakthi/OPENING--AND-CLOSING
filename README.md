## OPENING--AND-CLOSING
### Aim
To implement Opening and Closing using Python and OpenCV.

### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:
Import the necessary packages
#### Step2:
Create the Text using cv2.putText
#### Step3:
Create the structuring element
#### Step4:
Use Opening operation
#### Step5:
Use Closing Operation

### Program:
```
Developed by : YUVASAKTHI N.C 
Register Number:212222240120
```
#### Display the input Image
```py
import cv2
import numpy as np

img = np.zeros((350, 1400), dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img, 'ICE AGE', (15, 200), font, 5, (255), 10, cv2.LINE_AA)
cv2.imshow('created_text', img)
cv2.waitKey(0)
```
#### Create ths structured element
```py
struct_ele = np.ones((9, 9), np.uint8)
```
#### Display the result of Opening
```py
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, struct_ele)
cv2.imshow('Opening', opening)
cv2.waitKey(0)
```
#### Display the result of Closing
```py
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, struct_ele)
cv2.imshow('Closing', closing)
cv2.waitKey(0)
```
### Output:

#### Display the input Image
![image](https://github.com/IamShakthi/OPENING--AND-CLOSING/assets/117913445/1beedfe8-ad67-407c-8a9b-78fd4254aa04)



#### Display the result of Opening
![image](https://github.com/IamShakthi/OPENING--AND-CLOSING/assets/117913445/3fabcdd3-e20b-497f-acf4-3bb39484be39)



#### Display the result of Closing

![image](https://github.com/IamShakthi/OPENING--AND-CLOSING/assets/117913445/e1671092-f28a-4e5b-82f3-f8d15cbf2776)

### Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
