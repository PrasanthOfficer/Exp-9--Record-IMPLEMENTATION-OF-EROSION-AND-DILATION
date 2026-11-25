# Exp-9--Record-IMPLEMENTATION-OF-EROSION-AND-DILATION

# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:
- Image Erosion
- Image Dilation

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
Create a blank image using NumPy.

### Step 3:
Insert text onto the image using OpenCV's text drawing function.

### Step 4:
Display the original image.

### Step 5:
Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion
- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation
- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:
Compare the original, eroded, and dilated images.

## Program

```python
# Step 1: Import Libraries
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Step 2: Create a Blank Image
img = np.zeros((300, 500), dtype=np.uint8)

# Step 3: Insert Text into the Image
cv2.putText(
    img,
    "OPENCV",
    (50, 170),
    cv2.FONT_HERSHEY_SIMPLEX,
    2,
    255,
    5
)

# Step 4: Display Original Image
plt.figure(figsize=(12, 4))

plt.subplot(1, 3, 1)
plt.imshow(img, cmap="gray")
plt.title("Original Image")
plt.axis("off")

# Step 5: Create Structuring Element
kernel = np.ones((5, 5), np.uint8)

# Step 6: Image Erosion
erosion = cv2.erode(img, kernel, iterations=1)

plt.subplot(1, 3, 2)
plt.imshow(erosion, cmap="gray")
plt.title("Erosion")
plt.axis("off")

# Step 7: Image Dilation
dilation = cv2.dilate(img, kernel, iterations=1)

plt.subplot(1, 3, 3)
plt.imshow(dilation, cmap="gray")
plt.title("Dilation")
plt.axis("off")

# Step 8: Display Results
plt.tight_layout()
plt.show()
```

## Developed By

**Name:** Prasanth T

**Register No:** 212224040243

## Output

### Original Image
- A text image containing characters is displayed.
- The image serves as the input for morphological processing.
<img width="342" height="231" alt="image" src="https://github.com/user-attachments/assets/3f5ed305-548a-4e61-afcd-db88084085cd" />


### Erosion
- The thickness of the characters is reduced.
- Object boundaries shrink inward.
<img width="332" height="214" alt="image" src="https://github.com/user-attachments/assets/0d5c4fbf-1199-4bc7-8119-164597167b94" />


### Dilation
- The thickness of the characters increases.
- Object boundaries expand outward.
<img width="323" height="208" alt="image" src="https://github.com/user-attachments/assets/64f1646d-efdf-465b-bf23-d66345345fe7" />

  
## Result

Thus, the morphological operations **Erosion and Dilation** are successfully implemented using OpenCV.
