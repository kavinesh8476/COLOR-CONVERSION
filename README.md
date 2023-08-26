# COLOR-CONVERSION
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Import cv2 and save an image as scolor.jpeg.
<br>
### Step2:
Use imread to read and display the image.
<br>
### Step3:
Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.
<br>
### Step4:
Split and merge the image using cv2.split and cv2.merge commands.
<br>
### Step5:
End the program and view the output image windows.
<br>

## Program:
```python
# Developed By:Kavinesh M
# Register Number:212222230064
# READ AND DISPLAY THE IMAGE
import cv2
scolor=cv2.imread('aa.jpeg')
cv2.imshow('Original Image',scolor)
cv2.waitKey(0)
cv2.destroyAllWindows()

# i) Convert BGR and RGB to HSV and GRAY
#BGR2HSV
hsvimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsvimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#BGR2GRAY
grayimg=cv2.cvtColor(scolor,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',grayimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2HSV
hsvimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsvimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB2GRAY
grayimg2=cv2.cvtColor(scolor,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',grayimg2)
cv2.waitKey(0)
cv2.destroyAllWindows()


# ii)Convert HSV to RGB and BGR
#HSV TO RGB
rgbimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB',rgbimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

#HSV TO BGR
bgrimg=cv2.cvtColor(scolor,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR',bgrimg)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb
#BGR TO YCrCb
ybgr=cv2.cvtColor(scolor,cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb',ybgr)
cv2.waitKey(0)
cv2.destroyAllWindows()

#RGB TO YCrCb
yrgb=cv2.cvtColor(scolor,cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb',yrgb)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image
# SPLIT AND MERGE RGB IMAGE

blue=scolor[:,:,0]
green=scolor[:,:,1]
red=scolor[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()

# v) Split and merge HSV Image
# SPLIT AND MERGE HSV IMAGE
hsv = cv2.cvtColor(scolor, cv2.COLOR_BGR2HSV)
h,s,v=cv2.split(hsv)
cv2.imshow("Hue-image",h)
cv2.imshow("Saturation-image",s)
cv2.imshow("Gray-image",v)
Merged_HSV=cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()
```
## Output:
### Original image:
![originalimg](https://github.com/kavinesh8476/COLOR-CONVERSION/assets/118466561/3b74660d-ede7-48d5-8d90-e5eae5fd3758)

### 1. BGR and RGB to HSV and GRAY
### i) BGR TO HSV
![BGR2HSV](https://github.com/kavinesh8476/COLOR-CONVERSION/assets/118466561/5ac013d5-a014-4e6d-80e6-8e736dae8de5)
### ii) BGR TO GRAY
![BGR2GRAY](https://github.com/kavinesh8476/COLOR-CONVERSION/assets/118466561/28ac01db-dc97-4349-bee3-f2183142b432)
### iii) RGB TO HSV
![RGB2HSV](https://github.com/kavinesh8476/COLOR-CONVERSION/assets/118466561/e1e699fd-22b5-41fe-bb84-da153832c189)
### iv)RGB TO GRAY
![RGB2GRAY](https://github.com/kavinesh8476/COLOR-CONVERSION/assets/118466561/acb60073-034d-4b8d-b756-c60206080a49)

### 2. HSV to RGB and BGR
### i) HSV TO RGB
![HSV2RGB ](https://github.com/kavinesh8476/COLOR-CONVERSION/assets/118466561/6710cc26-1434-4492-b52b-e0c84a7b457c)
### ii) HSV TO BGR
![HSV2BGR](https://github.com/kavinesh8476/COLOR-CONVERSION/assets/118466561/2219cced-bce7-42fa-8b46-772aa58d2bc2)
### 3. RGB and BGR to YCrCb
### i) BGR TO YCrCb
![BGR2YCRCB](https://github.com/kavinesh8476/COLOR-CONVERSION/assets/118466561/410a3b46-0dd2-42ac-aade-26c4494b0b0f)
### ii) RGB TO YCrCb
![RGB2YCRCB](https://github.com/kavinesh8476/COLOR-CONVERSION/assets/118466561/42cdfb61-e591-4c8f-a454-509ca0c467c2)
### iv) Split and merge RGB Image

![SPL MRGRGB](https://github.com/kavinesh8476/COLOR-CONVERSION/assets/118466561/7dd5b9db-b3ad-4666-bfa7-19fa2592ff67)

### v) Split and merge HSV Image
![SPL MRGHSV](https://github.com/kavinesh8476/COLOR-CONVERSION/assets/118466561/3290f5b5-7215-4b4a-b238-230d2e7e6002)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
