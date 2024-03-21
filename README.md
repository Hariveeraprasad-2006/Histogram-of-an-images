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
# Developed By: 
# Register Number:
```
### Input Grayscale Image and Color Image
```
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('bookcover.jpg')
Color_image=cv2.imread('username.jpg')
plt.imshow(Gray_image)
plt.show()
plt.imshow(Color_image)
plt.show()
```
### Histogram of Grayscale Image and any channel of Color Image
```
import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('bookcover.jpg')
Color_image=cv2.imread('username.jpg')
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.imshow(Gray_image)
plt.show()
plt.title('Histogram')
plt.xlabel("grayscale value")
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title('Histogram')
plt.xlabel("grayscale value")
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```
# Code for Histogram Equalization of Grayscale Image.
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread('bookcover.jpg', cv2.IMREAD_GRAYSCALE)
equ = cv2.equalizeHist(image)
plt.imshow(Gray_image)
plt.show()
plt.imshow(equ)
plt.show()
```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/Hariveeraprasad-2006/Histogram-of-an-images/assets/145049988/0a612b21-6fc8-41c0-a188-d4e7e17476d4)


### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/Hariveeraprasad-2006/Histogram-of-an-images/assets/145049988/a893c80f-f9c1-4fe1-8167-d55b9db71901)
![image](https://github.com/Hariveeraprasad-2006/Histogram-of-an-images/assets/145049988/e86f3a0c-9bda-4106-a9db-e32978711ab4)



### Histogram Equalization of Grayscale Image.
![image](https://github.com/Hariveeraprasad-2006/Histogram-of-an-images/assets/145049988/5f3e2818-a68d-4769-860e-337cd19493e1)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
