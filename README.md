# Exp4-Histogram of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2 and matplotlib.pyplot.

### Step2:
Read and display the input images.

### Step3:
Calculate the Histogram Values using calcHist().

### Step4:
Display the histograms.

### Step5:
Calculate and display the equalized image using equalizeHist().
## Program:
```
Developed By: SASIDEVI V
Register Number: 212222230136
```
```
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

gray_image=cv2.imread('dog.jpg')
color_image=cv2.imread('fly.jpg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()



# Display the histogram of gray scale image and any one channel histogram from color image

gray_hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
color_hist=cv2.calcHist([color_image],[0],None,[256],[0,256])

plt.figure()
plt.title('Histogram')
plt.xlabel('Grayscale value')
plt.ylabel('pixel count')
plt.stem(gray_hist)
plt.show()

plt.title("Histogram")
plt.xlabel("Color Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()



# Write the code to perform histogram equalization of the image.

import cv2
gray_image=cv2.imread('dog.jpg',0)
gray_imageimage=cv2.resize(gray_image,(400,300))
equ = cv2.equalizeHist(gray_image)
cv2.imshow('Gray Image', gray_image)
cv2.imshow('Equalized Image', equ)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/SASIDEVIvenaram/HISTOGRAM/assets/118707332/d8b27880-89ff-4c22-b800-3a7a3a8162ed)

### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/SASIDEVIvenaram/HISTOGRAM/assets/118707332/2ce820ca-0078-4255-bc89-07d45a40fe97)

### Histogram Equalization of Grayscale Image

<img src="https://github.com/SASIDEVIvenaram/HISTOGRAM/assets/118707332/9f0fe032-063c-4b9f-8357-1dab5f79b357" width=500>

<img src="https://github.com/SASIDEVIvenaram/HISTOGRAM/assets/118707332/467a764f-a229-475c-915e-f2c1df810ee9" width=500>


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
