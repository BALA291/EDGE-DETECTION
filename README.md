# EX-06 EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.
## Program
```
DEVELOPED BY: BALAMURUGAN B
REGISTER NO: 212222230016
```

```
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("bala.png",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR

![6o](https://github.com/BALA291/EDGE-DETECTION/assets/120717501/353e5a78-bdfb-4060-bdc6-b265f39497a4)

![6oi](https://github.com/BALA291/EDGE-DETECTION/assets/120717501/0304533f-81e4-4c9c-b64c-121a3e660839)

![6oii](https://github.com/BALA291/EDGE-DETECTION/assets/120717501/a75a5d14-b85e-40a6-8e97-68c1c90f9747)


### LAPLACIAN EDGE DETECTOR

![6oiii](https://github.com/BALA291/EDGE-DETECTION/assets/120717501/09ad50c9-3337-49ee-9176-cd917a912f5d)

### CANNY EDGE DETECTOR
![6oiv](https://github.com/BALA291/EDGE-DETECTION/assets/120717501/279fc920-f872-4550-b287-8b037756c1b2)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
