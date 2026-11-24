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

**Name:** FARZANA M

**Register No:** 212225040087


### Original 
```
import cv2
import matplotlib.pyplot as plt

img = cv2.imread("bts.jpg")

if img is None:
    print("Error: Image not found. Check the file path.")
else:
    img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
    plt.imshow(img_rgb)
    plt.title("Original Image")
    plt.axis("off")
    plt.show()
```
<img width="771" height="442" alt="Screenshot 2026-11-24 203437" src="https://github.com/user-attachments/assets/e735fce3-2ab4-440e-9282-2e0c28202f60" />



### Original Grayscale Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("bts.jpg", cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap="gray")
plt.title("Original Grayscale Image")
plt.axis("off")
plt.show()
```
<img width="758" height="452" alt="Screenshot 2026-11-24 203444" src="https://github.com/user-attachments/assets/f349ea1d-4079-4d34-bff8-fb3060046b05" />


### Global Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("bts.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(img, 127, 255, cv2.THRESH_BINARY)
plt.imshow(result, cmap="gray")
plt.title("Global Thresholding")
plt.axis("off")
plt.show()
```
<img width="731" height="447" alt="Screenshot 2026-11-24 203451" src="https://github.com/user-attachments/assets/2ee49072-f8bd-46ad-a4a1-e7939d28c82e" />



### Adaptive Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("bts.jpg", cv2.IMREAD_GRAYSCALE)
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
<img width="735" height="448" alt="Screenshot 2026-11-24 203457" src="https://github.com/user-attachments/assets/7e7712ce-ca5a-4f15-ae7c-5ce0413cedb8" />


### Otsu's Thresholding
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("bts.jpg", cv2.IMREAD_GRAYSCALE)
_, result = cv2.threshold(
    img, 0, 255,
    cv2.THRESH_BINARY + cv2.THRESH_OTSU
)
plt.imshow(result, cmap="gray")
plt.title("Otsu's Thresholding")
plt.axis("off")
plt.show()
```
<img width="718" height="437" alt="Screenshot 2026-11-24 204304" src="https://github.com/user-attachments/assets/854037e8-2765-4f77-a7e2-32f13e2bc167" />



## Result

Thus, image segmentation is successfully performed using **Global Thresholding, Adaptive Thresholding, and Otsu's Thresholding** techniques in OpenCV. 
