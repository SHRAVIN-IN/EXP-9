# Implementation of Erosion and Dilation Using OpenCV
## Name : JANA SHRAVIN
## Regno : 212224243003
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

## Output

### Original Image
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("nature.jpeg")
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
```

<img width="546" height="522" alt="Screenshot 2026-09-02 214504" src="https://github.com/user-attachments/assets/67eebfb3-cce7-4858-942e-587b69951c84" />


### Erosion
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
erosion = cv2.erode(img, kernel, iterations=1)
plt.imshow(erosion, cmap="gray")
plt.title("Image Erosion")
plt.axis("off")
plt.show()
```
<img width="526" height="513" alt="Screenshot 2026-09-02 214513" src="https://github.com/user-attachments/assets/21ce082b-ed8c-40a7-a54e-7c8c089f1fa5" />



### Dilation
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
dilation = cv2.dilate(img, kernel, iterations=1)
plt.imshow(dilation, cmap="gray")
plt.title("Image Dilation")
plt.axis("off")
plt.show()
```

<img width="507" height="525" alt="Screenshot 2026-09-02 214524" src="https://github.com/user-attachments/assets/7dddced9-642e-4099-89a0-9b6920cfa965" />


## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
