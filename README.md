# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1: Load the necessary packages.

### Step2: Read the Image and convert to grayscale.

### Step3: Use Global thresholding to segment the image.

### Step4: Use Adaptive thresholding to segment the image.

### Step5: Use Otsu's method to segment the image and display the results

## Program

# Load the necessary packages

```
import cv2
import matplotlib.pyplot as plt
```

# Read the Image and convert to grayscale

```
image=cv2.imread("C:\\Users\\admin\\OneDrive\\Desktop\\DIPT\\flwr1.jpeg")
gray_img=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```

```
plt.subplot(2,2,1)
plt.imshow(cv2.cvtColor(image,cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```

```
_,global_thresholded = cv2.threshold(gray_img, 127, 255, cv2.THRESH_BINARY)

adaptive_thresholded = cv2.adaptiveThreshold(gray_img, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)

_,otsu_thresholded = cv2.threshold(gray_img, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

```


# Use Global thresholding to segment the image

```
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

```


# Use Adaptive thresholding to segment the image

```
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')

```

# Use Otsu's method to segment the image 

```
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

```
## Output

### Original Image


<img width="518" height="315" alt="Screenshot 2025-10-18 104018" src="https://github.com/user-attachments/assets/39da9928-4f9e-4675-81cb-90bc7adc38b9" />

### Global Thresholding



<img width="267" height="222" alt="Screenshot 2025-10-18 104037" src="https://github.com/user-attachments/assets/b63aeed4-fdba-4b2f-8a91-5d7c6a1f1dcd" />



### Adaptive Thresholding

<img width="337" height="312" alt="Screenshot 2025-10-18 104049" src="https://github.com/user-attachments/assets/071f7a8f-33fc-4907-a4e6-c31b24b38e57" />

### Optimum Global Thesholding using Otsu's Method


<img width="328" height="290" alt="Screenshot 2025-10-18 104054" src="https://github.com/user-attachments/assets/1c819f51-257b-4663-ac03-3317be62218d" />



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
