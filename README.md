# Edge-Detection-Opencv


## Aim

To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

---

## Software Required

- Anaconda – Python 3.7  
- Jupyter Notebook / VS Code  
- OpenCV (cv2)  
- NumPy  
- Matplotlib  

---

## ⚙️ Algorithm

### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load an image using `cv2.imread()`.

### Step 3:
Convert the image to grayscale.

### Step 4:
Apply **Original Image** using OpenCV to detect edges.

### Step 5:
Apply **Sobel Edge Detector** using custom kernels.

### Step 6:
Apply **Laplacian operator** using OpenCV.

### Step 7:
Apply **Canny edge detector** using OpenCV.

### Step 8:
Display all edge-detected images for comparison.

---

## Developed By

- **Name:** MADHUPRIYA R
- **Register No:** 212224040177

---

## Output

###  Original Image
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('dk_image.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="341" height="458" alt="image" src="https://github.com/user-attachments/assets/3f064ff2-3d99-4619-848c-c397a47dc31e" />



###  Sobel Edge Detector
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="338" height="457" alt="image" src="https://github.com/user-attachments/assets/9bf809d6-d1be-4fd9-90f2-9c11290bd675" />





###  Laplacian Edge Detector
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="331" height="458" alt="image" src="https://github.com/user-attachments/assets/5bdc7686-4d68-4e5f-97cf-eb751e062024" />



###  Canny Edge Detector
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
<img width="342" height="466" alt="image" src="https://github.com/user-attachments/assets/2df22d35-c65d-43c8-a9eb-3f6bfd945fc7" />


## Result

Thus, edges are successfully detected using Sobel, Prewitt, Roberts, Laplacian, and Canny edge detection techniques. Each method highlights edges differently based on gradient and intensity variations, improving feature extraction and analysis.
