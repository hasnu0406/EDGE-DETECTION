# Exp-6
# EDGE-DETECTION
### Developed by: HASNA MUBARAK AZEEM
### Register Number: 212223240052
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

### Developed by: HASNA MUBARAK AZEEM
### Register Number: 2122223240052

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('hasna.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
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
<img width="306" height="409" alt="download" src="https://github.com/user-attachments/assets/c42ad326-8878-4f32-95ef-5a8f7b613c2a" />

<img width="306" height="409" alt="download" src="https://github.com/user-attachments/assets/90ab8d2f-665d-48a8-ab90-4db73870a5ed" />

<img width="306" height="409" alt="download" src="https://github.com/user-attachments/assets/3d58c161-959e-433a-970c-c1040b960bd1" />

<img width="306" height="409" alt="download" src="https://github.com/user-attachments/assets/f9390bc5-16f6-4208-98bd-ed680493a60b" />





## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
