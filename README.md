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
```python
# Developed By: PRAGAHARSHITHA NC
# Register Number: 212222110033






```
## Output:
### Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("i1")
color_image = cv2.imread("i3",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Histogram of Grayscale Image and any channel of Color Image

```
import numpy as np
import cv2
Gray_image = cv2.imread("i1")
Color_image = cv2.imread("i3")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```

### Histogram Equalization of Grayscale Image.

```
import cv2
gray_image = cv2.imread("i1",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
nput Grayscale Image and Color Image:

![image](https://github.com/pragachellapillai/Histogram-of-an-images/assets/148254952/6b460be0-e87e-4930-9953-02d678e8f49c)

![image](https://github.com/pragachellapillai/Histogram-of-an-images/assets/148254952/a83b5b7e-39a9-4468-9138-5a2bb1f3d385)

Histogram of Grayscale Image and any channel of Color Image:

![image](https://github.com/pragachellapillai/Histogram-of-an-images/assets/148254952/81f0e0e6-8d5a-46a0-8928-16d21b8cf175)

![image](https://github.com/pragachellapillai/Histogram-of-an-images/assets/148254952/651e6f1c-d25a-4c07-ad39-aae21d2c5d1b)

![image](https://github.com/pragachellapillai/Histogram-of-an-images/assets/148254952/1f3793b1-459f-4090-bad2-707f3a592bfa)

![image](https://github.com/pragachellapillai/Histogram-of-an-images/assets/148254952/804dd57e-1d15-4061-92ed-90b1124de3c4)

Histogram Equalization of Grayscale Image.:

![image](https://github.com/pragachellapillai/Histogram-of-an-images/assets/148254952/43ed4fae-bc9b-4069-8b52-102325aa9336)

![image](https://github.com/pragachellapillai/Histogram-of-an-images/assets/148254952/f98da5cd-8837-4da3-b61b-caf7d9740eba)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
