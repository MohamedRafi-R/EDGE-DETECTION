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
### Developed By: R.Mohamed Rafi 
### Reg.No: 212224040195
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('Tiger.jpg')  # Replace with your image path
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

<img width="305" height="509" alt="Screenshot 2026-03-26 091747" src="https://github.com/user-attachments/assets/0076aa7f-1077-4c72-a126-6c8ab10154d3" />

<img width="299" height="513" alt="image" src="https://github.com/user-attachments/assets/5fa10689-8cb0-49da-a49c-caa381c89210" />

<img width="292" height="516" alt="image" src="https://github.com/user-attachments/assets/f3ace2ec-9a0d-40ae-a417-1339297ace67" />

<img width="312" height="522" alt="Screenshot 2026-03-26 091917" src="https://github.com/user-attachments/assets/88e7d284-130b-4e4b-8553-4817e607a27e" />




Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
