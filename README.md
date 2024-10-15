# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages.

### Step2:
Read the Image and convert to grayscale.

### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.

## Program

### Developed By: Yuvabharathi.B
### Register No.: 212222230181
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Read the image
image = cv2.imread('cute.jpeg')
# Convert to grayscale
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Display the original grayscale image
plt.imshow(gray_image, cmap='gray')
plt.title('Grayscale Image')
plt.xticks([]), plt.yticks([])
plt.show()
```
![Screenshot 2024-10-15 183323](https://github.com/user-attachments/assets/73ac9f7d-abe2-4499-8a38-02865db02aa8)

# Global thresholding
```
ret_global, th_global = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

# Display the global thresholding result
plt.imshow(th_global, cmap='gray')
plt.title('Global Thresholding (v=127)')
plt.xticks([]), plt.yticks([])
plt.show()

```
![Screenshot 2024-10-15 183332](https://github.com/user-attachments/assets/5c958ce2-fcd9-4e37-b71e-4dd563fcfbdf)

# Adaptive thresholding (Gaussian)
```
th_adaptive = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY, 11, 2)
# Display the adaptive thresholding result
plt.imshow(th_adaptive, cmap='gray')
plt.title('Adaptive Gaussian Thresholding')
plt.xticks([]), plt.yticks([])
plt.show()
```
![Screenshot 2024-10-15 183340](https://github.com/user-attachments/assets/a488f2e9-ac99-45e0-b351-9a3985136214)

# Otsu's thresholding
```
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
# Display the Otsu thresholding result
plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()
```
![Screenshot 2024-10-15 183349](https://github.com/user-attachments/assets/0ab03257-31ba-4c05-85d8-15a557714587)

## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
