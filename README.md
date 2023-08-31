# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
```python
# Developed By:SHARMILA
# Register Number:212221230094
```

import cv2
import matplotlib.pyplot as plt
Gray_image=cv2.imread('fro.png')
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread('dip1.jpeg')
plt.imshow(Color_image)
plt.show()

# Write your code to find the histogram of gray scale image and color image channels.
```
hist=cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("gray_scale value")
plt.ylabel("pixel count")
plt.stem(hist)
plt.show()
```
# Display the histogram of gray scale image and any one channel histogram from color image
```
hist1=cv2.calcHist([Color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel("color_scale value")
plt.ylabel("pixel count")
plt.stem(hist1)
plt.show()
```
# Write the code to perform histogram equalization of the image. 
```
equ=cv2.equalizeHist(cv2.imread('dip1.jpeg',0))
equ=cv2.cvtColor(equ,cv2.COLOR_BGR2RGB)
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ)
plt.show()




```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>
<br>

### ii) HSV to RGB and BGR
<br>
<br>

### iii) RGB and BGR to YCrCb
<br>
<br>

### iv) Split and merge RGB Image
<br>
<br>

### v) Split and merge HSV Image
<br>
<br>


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
