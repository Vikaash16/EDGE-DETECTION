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
<img width="608" height="345" alt="image" src="https://github.com/user-attachments/assets/300065a0-9430-4b09-bc12-4675889d2527" />


### LAPLACIAN EDGE DETECTOR
<img width="624" height="332" alt="image" src="https://github.com/user-attachments/assets/abadc007-80f3-49ca-8690-48b109418299" />


### CANNY EDGE DETECTOR
<img width="542" height="339" alt="image" src="https://github.com/user-attachments/assets/79d5e872-4962-494e-9e83-2bf1f33e4f67" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
