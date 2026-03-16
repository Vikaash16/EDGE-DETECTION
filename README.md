# EDGE-DETECTION
## NAME : Vikaash P
## REG NO : 212223240

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

### Program
```PYTHON
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('TK.JPG')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
## Output:
### SOBEL EDGE DETECTOR
<img width="724" height="440" alt="image" src="https://github.com/user-attachments/assets/a52fd56b-3f95-4b96-b15b-5be255a7ca44" />



### LAPLACIAN EDGE DETECTOR
<img width="716" height="445" alt="image" src="https://github.com/user-attachments/assets/9ae38f99-e563-47a8-aab8-df17d7dfb0af" />



### CANNY EDGE DETECTOR
<img width="770" height="432" alt="image" src="https://github.com/user-attachments/assets/0ed740dc-1413-4bee-b3d9-cf14831a15b5" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
