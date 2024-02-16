# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

##### Program:
### Developed By: ATHMAJ VENUGOPAL
### Register Number: 212222240014


## Output:

### i) Read and display the image
```py
    import cv2
    image=cv2.imread('car.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Athmaj Venugopal',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## Output:
![one](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/438e6aa6-5479-4ba2-b649-0e8a13588081)


### ii)Write the image
```py
    import cv2
    image=cv2.imread('car.jpg',0)
    cv2.imwrite('vintage.jpg',image)
```
## Output:
![two](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/99db2583-0a28-43c9-9a1d-a0c1d0ce6eeb)


### iii)Shape of the Image
```py
    import cv2
    image=cv2.imread('car.jpg',1)
    print(image.shape)
```
## Output:
![three](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/5e329a07-087d-4347-a0f7-da30b54269ec)

### iv)Access rows and columns
```py
    import random
    import cv2
    image=cv2.imread('car.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
## Output:
![four](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/cbcbeade-b65a-44b4-9acf-eaeadcb0c49b)


### v)Cut and paste portion of image
```py
   import cv2
   image=cv2.imread('car.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('partimage1',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
## Output:
![five](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/e7957481-5005-4e27-8605-f62357ff9c27)

### vi) BGR and RGB to HSV and GRAY
```py
import cv2
img = cv2.imread('car.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![six](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/1f8c88ea-648d-4077-a4b1-ecad2d434fcc)
![seven](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/07da308e-7234-49e0-92d1-f299d03a563a)
![eight](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/81c165aa-bd05-490e-95bb-516dd624e1d0)
![nine](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/df13f26f-374e-4df6-a98f-003fd3aa84c2)
![ten](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/8dc62b20-6241-4fc7-8510-67365bdb4caa)

### vii) HSV to RGB and BGR
```py
import cv2
img = cv2.imread('car.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![eleven](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/aba2f508-c330-40d4-95b6-0438d5249f38)
![twelve](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/b690c9dc-cddf-4d28-b6ac-2975222b00c5)
![thirteen](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/9340045f-5744-456b-b973-93e8b0fcf79d)

### viii) RGB and BGR to YCrCb
```py
import cv2
img = cv2.imread('car.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![fourteen](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/a8fbce25-1f7e-4b5a-b987-339eaf22c872)
![fifteen](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/45f7d4a5-4269-40cd-b33d-a93c490d8864)
![sixteen](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/a2f32b13-42cf-4fd0-8b70-3456a594bbb1)

### ix) Split and merge RGB Image
```py
import cv2
img = cv2.imread('car.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![seventeen](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/7cd3be7b-07f0-41e9-b5c9-61a08dd2ac76)
![eighteen](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/d6e573e4-cde2-4786-b02e-831e7ab38bf5)
![nineteen](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/36e98a35-64fd-49c9-983e-c8ff3ee9daa9)
![twenty](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/100e3565-4ba4-401b-bb5a-1fbecb17411f)

### x) Split and merge HSV Image
```py
import cv2
img = cv2.imread("car.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
![twentyone](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/a0ad9de3-be3f-4fab-8961-30f3d7b10fa8)
![twentytwo](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/7a977bdf-495c-4fda-9922-cfa0e9dc4a45)
![twentythree](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/05372028-b64a-4ead-aea1-562d2810b7e0)
![twentyfour](https://github.com/ATHMAJ03/COLOR_CONVERSIONS_OF-IMAGE/assets/118753139/fafb8fef-727b-4fdc-9fc1-3533c827cb21)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







