# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save and image as filename.jpg

### Step2:
Use imread(filename, flags) to read the file.

### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:

Split and merge the image using cv2.split and cv2.merge commands.

### Step5:
End the program and close the output image windows.

## Program:
```python
# Developed By:SHARMILA
# Register Number:212221230094
```
```
import cv2
img=cv2.imread('mo.jpg')
cv2.imshow('Org_img',img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Write your code to find the histogram of gray scale image and color image channels.
```
hsv_img=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

hsv_img1=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_img1)
cv2.waitKey(0)
cv2.destroyAllWindows()

gray_img=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

gray_img1=cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_img1)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Display the histogram of gray scale image and any one channel histogram from color image
```
rgb_img=cv2.cvtColor(hsv_img,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV to RGB',rgb_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

bgr_img=cv2.cvtColor(hsv_img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to BGR',bgr_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
# Write the code to perform histogram equalization of the image. 
```
YCrCb_1 = cv2.cvtColor(rgb_img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('YCrCb_1',YCrCb_1)
cv2.waitKey(0)
cv2.destroyAllWindows()

YCrCb_2 = cv2.cvtColor(bgr_img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('YCrCb_2',YCrCb_2)
cv2.waitKey(0)
cv2.destroyAllWindows()
blue = img[:,:,0]
green = img[:,:,1]
red = img[:,:,2]
cv2.merge((blue,green,red))
h, s, v = cv2.split(hsv_img)
cv2.merge((h,s,v))


```
## Output:
### i) BGR and RGB to HSV and GRAY
![dip 3 2](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/57c9b24a-6390-4d5d-9c0d-6dda617d80c3)
![dipp 3 3](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/e5ac2974-764e-4fb0-b59f-402732a2ab42)
![dip 3 4](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/7e6a9f23-f1eb-4a9f-a14e-d534765d5d5e)
![dip 3 5](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/78d70645-4ddd-4b8c-b7b8-5246e7428038)

### ii) HSV to RGB and BGR
![dip 3 6](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/93a9e5c6-b5d3-439b-a178-d9b0de2fdc7a)
![dip 3 7](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/b5f78eda-07fa-456e-9db0-eae1ff6b2c4b)

### iii) RGB and BGR to YCrCb
![dip 3 8](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/4273f290-42ab-4dc4-950c-16a49b603527)
![dip 3 9](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/d0394f4b-9207-4cf1-97c7-66009701c277)


### iv) Split and merge RGB Image
![dip 3 10](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/7bc9dfef-58fd-4894-b743-02d7c12ebd7d)
![dip 3 11](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/6bb4894a-edfe-4cc9-b484-bcf5a52866e6)



### v) Split and merge HSV Image
![dip 3 11](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/6bb4894a-edfe-4cc9-b484-bcf5a52866e6)

![dip  3 12](https://github.com/Sharmilasha/COLOR-CONVERSION/assets/94506182/77dc9551-575b-4a68-b84b-76c362ae25a4)

## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
