# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read two images, Color image and Gray Scale image.

### Step2:
Calculate the Histogram of Gray scale image and any one channel of the color image

### Step3:
Display the histograms.

### Step4:
Equalize the grayscale image

### Step5:
Display the equalized grayscale image

## Program:
```python
# Developed By:Swetha.K.P
# Register Number:212220230053
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('chota.jpg')
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread('img1.jpg')
plt.imshow(Color_image)
plt.show()

# Write your code to find the histogram of gray scale image and color image channels.
hist1 = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('color_scale value')
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image
hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('gray_scale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

# Write the code to perform histogram equalization of the image. 
equ=cv2.equalizeHist(cv2.imread('chota.jpg',0))
equ=cv2.cvtColor(equ,cv2.COLOR_BGR2RGB)
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ)
plt.show()
```
## Output:
### Input Grayscale Image and Color Image
![dip 31](https://user-images.githubusercontent.com/75235209/165315485-575f299d-f76d-4597-a5a7-1064e88cfa17.PNG)

### Histogram of Grayscale Image and any channel of Color Image
![dip 32](https://user-images.githubusercontent.com/75235209/165315560-0774dd35-0855-4cd1-8fd4-0dd53e2b4b8e.PNG)


### Histogram Equalization of Grayscale Image
![dip 33](https://user-images.githubusercontent.com/75235209/165315612-b2b57e8e-d47e-4441-9e62-619fff950d8b.PNG)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
