# DIPT_EXP_8
# Image Segmentation Using Thresholding Techniques in OpenCV

## Aim

To segment an image using Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding techniques using Python and OpenCV.

The program performs the following operations:

- Global Thresholding
- Adaptive Thresholding
- Otsu's Thresholding

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Load the input image using OpenCV.

### Step 3:

Convert the input image into grayscale format.

### Step 4: Global Thresholding

- Select a fixed threshold value.
- Apply thresholding to separate foreground and background pixels.
- Display the thresholded image.

### Step 5: Adaptive Thresholding

- Compute threshold values for small regions of the image.
- Apply Adaptive Mean Thresholding.
- Apply Adaptive Gaussian Thresholding.
- Display the segmented images.

### Step 6: Otsu's Thresholding

- Automatically determine the optimal threshold value.
- Apply Otsu's thresholding technique.
- Display the segmented image.

### Step 7:

Compare the results obtained from Global, Adaptive, and Otsu's thresholding methods.

## Program

## Developed By

**Name:** POOJA PRIYA B

**Register No:** 212224230196


### Original 
```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("tulip.jpg")

if img is None:
    print("Error: Image not found. Check the file path.")
else:
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    plt.imshow(img_rgb)
    plt.title("Original Image")
    plt.axis("off")
    plt.show()
```
<img width="306" height="391" alt="image" src="https://github.com/user-attachments/assets/01ac448a-d321-4c61-a19e-ab85ae5e6092" />


### Original Grayscale Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("tulip.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```
<img width="383" height="395" alt="image" src="https://github.com/user-attachments/assets/1f7984dc-2428-4637-8a4d-22e11a13c92d" />

### Global Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("tulip.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```
<img width="361" height="392" alt="image" src="https://github.com/user-attachments/assets/20049596-1ad7-4e17-92f2-5d6189f2959f" />



### Adaptive Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("tulip.jpg", cv2.IMREAD_GRAYSCALE)
result = cv2.adaptiveThreshold(
    img, 255,
    cv2.ADAPTIVE_THRESH_GAUSSIAN_C,
    cv2.THRESH_BINARY,
    11, 2
)
plt.imshow(result, cmap="gray")
plt.title("Adaptive Thresholding")
plt.axis("off")
plt.show()
```
<img width="367" height="376" alt="image" src="https://github.com/user-attachments/assets/692ed932-2b1b-4229-9152-46beef753ea2" />

### Otsu's Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("tulip.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```
<img width="477" height="376" alt="image" src="https://github.com/user-attachments/assets/a8e6924a-cbab-40b8-918e-85c2dd120ae4" />


## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
