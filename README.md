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

#### Developed By: HARINI V
#### Register Number: 212222230044
### Input Grayscale Image and Color Image:
```python
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread('tree.jpg')
Color_image = cv2.imread('york.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()
```
### Histogram of Grayscale Image and Green channel of Color Image:
```python
hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('grayscale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram of Color Image Green Channel")
plt.xlabel('Intensity value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```
### Histogram Equalization of Grayscale Image:
```python
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
```
## Output:
### Input Grayscale Image and Color Image:
![image](https://github.com/harini1006/Histogram-of-an-images/assets/113497405/96013a5b-1b0c-496c-916b-c42975d8984e)
![image](https://github.com/harini1006/Histogram-of-an-images/assets/113497405/9b555a44-45ee-459f-b73b-91dff24639fa)



### Histogram of Grayscale Image and any channel of Color Image

![image](https://github.com/harini1006/Histogram-of-an-images/assets/113497405/357270c2-b24f-4bae-9447-8841d0d780f4)
![image](https://github.com/harini1006/Histogram-of-an-images/assets/113497405/ab2383c0-3cd8-4cb7-b209-e748fe85dd55)


### Histogram Equalization of Grayscale Image.
![image](https://github.com/harini1006/Histogram-of-an-images/assets/113497405/dacf9871-e51f-4642-8efe-38c5e36aace8)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
