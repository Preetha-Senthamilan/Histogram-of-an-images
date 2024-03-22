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
# Developed By: PREETHA.S
# Register Number: 212222230110

### Grayscale and colour image
```
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cat.jpg")
color_image = cv2.imread("bird.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Histogram of grayscale
```
import numpy as np
import cv2
Gray_image = cv2.imread("img1.jpeg")
Color_image = cv2.imread("img.jpg")
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

### Histogram of Color image
```
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
### Histogram equalization of Grayscale image
```

import cv2
gray_image = cv2.imread("bird.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


## Output:
### Input Grayscale Image and Color Image

![Screenshot 2024-03-22 143118](https://github.com/Preetha-Senthamilan/Histogram-of-an-images/assets/119390282/4fd2595e-9e42-42ef-9743-d41642c7d82d)

![Screenshot 2024-03-22 143135](https://github.com/Preetha-Senthamilan/Histogram-of-an-images/assets/119390282/ca928d8e-1db5-4578-9c93-587e195cf1e4)


### Histogram of Grayscale Image 

![image](https://github.com/Preetha-Senthamilan/Histogram-of-an-images/assets/119390282/80496098-4148-4618-962d-bd291aee2aa8)

![image](https://github.com/Preetha-Senthamilan/Histogram-of-an-images/assets/119390282/38a28999-dd51-40c1-a4e1-d3e9edfc7664)

### Histogram of Color image

![image](https://github.com/Preetha-Senthamilan/Histogram-of-an-images/assets/119390282/37781416-8424-47bb-8ded-31caeaa27147)

![image](https://github.com/Preetha-Senthamilan/Histogram-of-an-images/assets/119390282/d37e52e6-9606-4983-adec-ce2e142d7e85)


### Histogram Equalization of Grayscale Image.

![Screenshot 2024-03-22 204841](https://github.com/Preetha-Senthamilan/Histogram-of-an-images/assets/119390282/d5a1e114-701d-472c-8872-9b694996017e)  ![Screenshot 2024-03-22 204858](https://github.com/Preetha-Senthamilan/Histogram-of-an-images/assets/119390282/218d8d89-cd06-4400-9e8b-e66753b96dea)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
