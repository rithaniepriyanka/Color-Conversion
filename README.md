# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
```python
Read an image using imread() and Convert BGR and RGB to HSV and GRAY
using:
cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
```
### Step2:
```python
Convert HSV to RGB and BGR
using:
cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
```
### Step3:
```python
Convert RGB and BGR to YCrCb
using:
cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
```
### Step4:
```python
Split and Merge RGB Image
using:
blue = image[:,:,0]
green = image[:,:,1]
red = image[:,:,2]
cv2.merge((blue,green,red))
```
### Step5:
```python
Split and merge HSV Image
using:
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.merge((h,s,v))
```

## Program:
```python
# Developed By: RITHANIEPRIYANKA . J
# Register Number: 212220230039
# i) Convert BGR and RGB to HSV and GRAY

import cv2
image=cv2.imread("rithu2.jpg")
cv2.imshow("212220230008",image)
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR to HSV image",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR to GRAY image",BGR_GRAY)
RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB to HSV image",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB to GRAY image",RGB_GRAY)
cv2.imshow("rithu2",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# ii)Convert HSV to RGB and BGR

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV image",hsv)
HSV_RGB=cv2.cvtColor(image,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV to RGB image",HSV_RGB)
HSV_BGR=cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV to BGR image",HSV_BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iii)Convert RGB and BGR to YCrCb

RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB to YCrCb image",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR to YCrCb image",BGR_YCrCb)
cv2.imshow("rithu2",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# iv)Split and Merge RGB Image

blue = image[:,:,0]
cv2.imshow("Blue Split",blue)
green = image[:,:,1]
cv2.imshow("Green Split",green)
red = image[:,:,2]
cv2.imshow("Red Split",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("Merged Image",merged)
cv2.imshow("212220230008",image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# v) Split and merge HSV Image

hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow("HSV image",hsv)
cv2.imshow('Merged HSV',mergedhsv)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:

### i) BGR and RGB to HSV and GRAY
![3a1](https://user-images.githubusercontent.com/75235132/163558150-d977cf3d-6862-4c23-949b-9231050171d7.png)
![3a2](https://user-images.githubusercontent.com/75235132/163558161-10ad2237-0679-4daf-a7a9-3410ef259e50.png)
![3b](https://user-images.githubusercontent.com/75235132/163558174-45561281-f614-4891-8eba-94d7e465022a.png)
### ii) HSV to RGB and BGR
![3c](https://user-images.githubusercontent.com/75235132/163558216-227868ec-10c4-4e39-b0db-49e8558d0162.png)
### iii) RGB and BGR to YCrCb
![3 III](https://user-images.githubusercontent.com/75235132/163558238-8ccb2454-2c27-44ae-99f7-6475fc3c4a4c.png)
### iv) Split and merge RGB Image
![3d](https://user-images.githubusercontent.com/75235132/163558228-a353d7d1-5b35-4f1b-969d-206fbcb4c0f7.png)
![3d1](https://user-images.githubusercontent.com/75235132/163558297-93673daa-5a1d-4757-8e99-447246d918aa.png)
### v) Split and merge HSV Image
![3e](https://user-images.githubusercontent.com/75235132/163558310-0fc6a82a-8728-4bf1-bf98-96c3829be6da.png)
![3e1](https://user-images.githubusercontent.com/75235132/163558352-329ae7a5-74a6-4fc7-9ba8-c2794091caa3.png)
## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
