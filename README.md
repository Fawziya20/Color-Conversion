# Color Conversion
## AIM

To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:

### Step1:
Import cv2 library and upload the image or capture an image.
<br>

### Step2:
Read the saved image using cv2.imread("filename.jpg").
<br>

### Step3:
Convert the image into the given color transformation using cv2.cvtColor(image, cv2.BGR2YCrCb) 
and similarly for other color formats. 
<br>

### Step4:
Split and merge the image using cv2.split(hsv) and cv2.merge([h,s,v]) 
<br>

### Step5:
Output the image using cv2.imshow("OUTPUT", image)

<br>

## Program:

### Developed By: FAWZIYA A
### Register Number: 212220230017

## i) Convert BGR and RGB to HSV and GRAY

```python

# (i) bgr and rgb to hsv and gray

import cv2
house_color_image = cv2.imread('hp3.png')
cv2.imshow('original image',house_color_image)
hsv_image = cv2.cvtColor(house_color_image,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv_image)
hsv_image1 = cv2.cvtColor(house_color_image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv_image1)
gray_image = cv2.cvtColor(house_color_image,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray_image)
gray_image1 = cv2.cvtColor(house_color_image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray_image1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## ii)Convert HSV to RGB and BGR

```python

# (ii)Convert HSV to RGB and BGR

import cv2
img = cv2.imread("hp1.jpg")
img1= cv2.resize(img, (270,190))
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
hsv_rgb = cv2.cvtColor(hsv, cv2.COLOR_HSV2RGB)
cv2.imshow("HSV2RGB", hsv_rgb)
hsv_bgr = cv2.cvtColor(hsv, cv2.COLOR_HSV2BGR)
cv2.imshow("HSV_BGR", hsv_bgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## iii)Convert RGB and BGR to YCrCb

```python 

# (iii)convert RGB and BGR to YCrCb

import cv2
img = cv2.imread("hp3.png")
img1= cv2.resize(img, (270,190))
cv2.imshow("BGR_COLOR ", img1)
img_ycrcb = cv2.cvtColor(img1 , cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR_YCRCB ", img_ycrcb)
img_bgr = cv2.cvtColor(img1, cv2.COLOR_BGR2RGB)
cv2.imshow("RGB COLOR", img_bgr)
img_bgr_y = cv2.cvtColor(img_bgr, cv2.COLOR_BGR2YCrCb)
cv2.imshow("RGB2YCrCb", img_bgr_y)
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## iv)Split and Merge RGB Image
```python 

# (iv) Split and Merge RGB Image

import cv2
img = cv2.imread("hp1.jpg")
img1= cv2.resize(img, (270,190))
cv2
b,g,r = cv2.split(img1)
cv2.imshow("RED MODEL", r)
cv2.imshow("GREEN MODEL", g)
cv2.imshow("BLUE MODEL ", b)
merger = cv2.merge([b,g,r])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## v) Split and merge HSV Image

```python 


# (v)Split and merge HSV Image

import cv2
img = cv2.imread("hp3.png")
img1= cv2.resize(img, (270,190))
hsv = cv2.cvtColor(img1 , cv2.COLOR_BGR2HSV)
cv2.imshow("INITIAL_HSV ", hsv)
h,s,v = cv2.split(hsv)
cv2.imshow("RED MODEL", h)
cv2.imshow("GREEN MODEL", s)
cv2.imshow("BLUE MODEL ", v)
merger = cv2.merge([h,s,v])
cv2.imshow("MERGED IMAGE", merger )
cv2.waitKey(0)
cv2.destroyAllWindows()

```

## Output:
### i) BGR and RGB to HSV and GRAY
<br>
![image](https://user-images.githubusercontent.com/75235022/162606151-b114a492-0607-4b78-b172-51c46bc5600c.png)





<br>

### ii) HSV to RGB and BGR
<br>
![image](https://user-images.githubusercontent.com/75235022/162606209-3444bf6d-4aca-4054-b2b2-e6ab5be2cb2d.png)





<br>

### iii) RGB and BGR to YCrCb
<br>
![image](https://user-images.githubusercontent.com/75235022/162606301-fbbdf855-e03e-49fa-848a-4d62a6138992.png)





<br>

### iv) Split and merge RGB Image
<br>
![image](https://user-images.githubusercontent.com/75235022/162606357-bc0528eb-7884-49c3-8f1a-b25adf9585bd.png)






<br>

### v) Split and merge HSV Image
<br>
![image](https://user-images.githubusercontent.com/75235022/162606380-990e9f2c-94a8-438b-adf1-400408c176b3.png)





<br>



## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
