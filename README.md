# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program:
```
Developed BY:VARSHINI D
Reg No:212223230234


import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('Documents/DIPT/fort.jpg')  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)
sobel_combined = cv2.magnitude(sobel_x, sobel_y)
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
plt.show()
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
plt.show()
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR

![image](https://github.com/user-attachments/assets/fde992c1-2c1d-46f9-ad44-e03de0e69e7c)



### LAPLACIAN EDGE DETECTOR

![image](https://github.com/user-attachments/assets/1e214066-512a-463a-975d-2f732a76e7cf)



### CANNY EDGE DETECTOR

![image](https://github.com/user-attachments/assets/829121cd-0e52-492e-8d47-6b5e4fe7df46)



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
