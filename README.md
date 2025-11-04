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
### ORIGINAL IMAGE
```
NAME : NARESH.M
REG NO : 212223220064



import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('nar.jpg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### ORIGINAL IMAGE
<img width="692" height="897" alt="{90CFC966-8458-43AA-8FEB-D80F45503292}" src="https://github.com/user-attachments/assets/cf525e1b-bc21-400a-a85e-8df9be59ed0c" />



### SOBEL EDGE DETECTOR
<img width="729" height="899" alt="{87549376-E56B-4718-ABB9-48E0D87CB2A3}" src="https://github.com/user-attachments/assets/e6afe406-49e5-49a4-a88f-a0413ca6b5ae" />




### LAPLACIAN EDGE DETECTOR
<img width="724" height="883" alt="{FDC6921D-63D2-49ED-B04B-0B4FD307B539}" src="https://github.com/user-attachments/assets/779b0147-b31b-4c8e-8eb2-5af4587c1d01" />




### CANNY EDGE DETECTOR
<img width="741" height="899" alt="{6E3DE98A-7C33-431D-98D7-CF636F034120}" src="https://github.com/user-attachments/assets/0357b7b5-3dd5-4264-859e-45e41d7717df" />




## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
