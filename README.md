# Histogram-of-an-images

## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: YASHWINI M
# Register Number: 212223230249
```



## Histogram of Grayscale Image

```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
img = cv2.imread('parrot.jpg', cv2.IMREAD_GRAYSCALE)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.show()plt.hist(img.ravel(),256,range = [0, 256]);
plt.title('Original Image')
plt.show()
plt.hist(img.ravel(),256,range = [0, 256]);
plt.title('Histogram of Original Image')
plt.show()
img_eq = cv2.equalizeHist(img)
plt.hist(img_eq.ravel(), 256, range = [0, 256])
plt.title('Equalized Histogram')

```

## Output:

<img width="712" height="413" alt="image" src="https://github.com/user-attachments/assets/b3edc61e-8d42-4e47-ba65-19558542714b" />

<img width="724" height="545" alt="image" src="https://github.com/user-attachments/assets/0b2c18c2-7e42-42b6-bb35-4daca419a8b6" />

<img width="725" height="549" alt="image" src="https://github.com/user-attachments/assets/8d4e71db-abb0-4e55-92cb-116e21cfa231" />


## Histogram of Color Image
``` python
img = cv2.imread('parrot.jpg', cv2.IMREAD_COLOR)
img_hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
img_hsv[:,:,2] = cv2.equalizeHist(img_hsv[:, :, 2])
img_eq = cv2.cvtColor(img_hsv, cv2.COLOR_HSV2BGR)
plt.imshow(img_eq[:,:,::-1]); 
plt.title('Equalized Image');
plt.show()
plt.hist(img_eq.ravel(),256,range = [0, 256]);
plt.title('Histogram Equalized');
plt.show()

```

## OUTPUT

<img width="719" height="419" alt="image" src="https://github.com/user-attachments/assets/0824af26-c4bd-45a1-807b-34cee5e0d553" />

<img width="706" height="414" alt="image" src="https://github.com/user-attachments/assets/2cd64e72-bc69-4571-92e8-543028fadd4d" />

<img width="732" height="549" alt="image" src="https://github.com/user-attachments/assets/58dc351e-0d2b-463c-83e5-a9177f1c4255" />


## Histogram Equilization of GrayScale Image
``` python
import cv2
import numpy as np
import matplotlib.pyplot as plt
img = cv2.imread('parrot.jpg', cv2.IMREAD_GRAYSCALE)
plt.subplot(221); plt.imshow(img[:, :, ::-1]); plt.title('Original Color Image')
plt.subplot(222); plt.imshow(img_eq[:, :, ::-1]); plt.title('Equalized Image')
plt.subplot(223); plt.hist(img.ravel(),256,range = [0, 256]); plt.title('Original Image')
plt.subplot(224); plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized');plt.show()
plt.figure(figsize = [15,4])
plt.subplot(121); plt.hist(img.ravel(),256,range = [0, 256]); plt.title('Original Image')
plt.subplot(122); plt.hist(img_eq.ravel(),256,range = [0, 256]); plt.title('Histogram Equalized')
```

## OUTPUT

<img width="723" height="514" alt="image" src="https://github.com/user-attachments/assets/bf41fd29-dccd-4a31-8c84-e393708a85bf" />

<img width="785" height="243" alt="image" src="https://github.com/user-attachments/assets/0a7cfa7b-2bd5-4abc-873c-24354eae7c46" />

## RESULT
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
