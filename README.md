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
 Developed By: JB JERUSHLIN JOSE
 Register Number: 212222240039
```
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("THALA.png")
color_image = cv2.imread("THALAPATHY.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
import numpy as np
import cv2
Gray_image = cv2.imread("THALA.jpg")
Color_image = cv2.imread("THALAPATHY.jpg")
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
```
```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
```python
import cv2
gray_image = cv2.imread("THALA.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```







## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/Jerushli/Histogram-of-an-images/assets/120041243/97f8d24d-0483-403b-b7a1-413939328a67)


### Histogram of Grayscale Image and any channel of Color Image

#### Grayscale Image
![image](https://github.com/Jerushli/Histogram-of-an-images/assets/120041243/5e9d0d28-893b-43f4-b6d7-717d3c60e372)

#### Color Image

![image](https://github.com/Jerushli/Histogram-of-an-images/assets/120041243/248a4c77-9261-4ffc-b385-1464c0e018a8)


### Histogram Equalization of Grayscale Image.

![image](https://github.com/Jerushli/Histogram-of-an-images/assets/120041243/5bf69cad-2daa-4f7c-96ef-4b9f339cd07a)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
