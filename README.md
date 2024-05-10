# EXP-01:COLOR_CONVERSIONS_OF-IMAGE
# DATE:
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
### Developed By:
### Register Number: 


## Output:

### i) Read and display the image
```
    import cv2
    image=cv2.imread('cows.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('Shabreena Vincent',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
### OUTPUT:
![SHABREENA](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/1d56a08e-aab6-40da-9d4f-3bbed7ca07c6)
### ii)Write the image
```
    import cv2
    image=cv2.imread('cows.jpg',0)
    cv2.imwrite('image.jpg',image)
```
### OUTPUT:
![OUTPUT2](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/bd913a9c-6ccc-4e8c-84e8-0c422ce746ae)
### iii)Shape of the Image
```
    import cv2
    image=cv2.imread('cows.jpg',1)
    print(image.shape)
```
### OUTPUT:
![OUTPUT3](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/c135fa09-3f4a-4f5b-bcd8-21b3da57d5f3)
### iv)Access rows and columns
```
    import random
    import cv2
    image=cv2.imread('cows.jpg',1)
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
### OUTPUT:
![Screenshot 2024-02-22 202716](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/4a766ee6-cf72-4262-b701-f22e2781e967)
### v)Cut and paste portion of image
```
   import cv2
   image=cv2.imread('cows.jpg',1)
   image=cv2.resize(image,(400,400))
   tag =image[130:200,110:190]
   image[110:180,120:200] = tag
   cv2.imshow('partimagecow',image)
   cv2.waitKey(0)
   cv2.destroyAllWindows()
```
### OUTPUT:
![Screenshot 2024-02-22 202848](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/032ca77f-d29d-474d-9536-6ddf5f33a350)
### vi) BGR and RGB to HSV and GRAY
```
import cv2
img = cv2.imread('cows.jpg',1)
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
### OUTPUT:
![Screenshot 2024-02-22 202956](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/35c0dfcf-e131-4d9b-b8a9-32545b9adeeb)
![Screenshot 2024-02-22 203004](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/3bdb311b-c4b2-4708-9f1c-1736c160b250)
![Screenshot 2024-02-22 203013](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/56e91420-bd85-407d-b2f2-6db01068e65e)
![Screenshot 2024-02-22 203019](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/b09d5b90-e672-4550-a4a4-3f4bafc0c161)
![Screenshot 2024-02-22 203026](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/550e19d0-b6cb-4eeb-a52c-e77759cf7b64)
![Screenshot 2024-02-22 203032](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/60bcf646-542f-4b1c-a8f2-058880ab3a3c)
### vii) HSV to RGB and BGR
```
import cv2
img = cv2.imread('cOWS.jpg')
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
### OUTPUT:
![Screenshot 2024-02-22 203113](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/9b4014e7-f3ae-4866-a851-7205e81d0661)
![Screenshot 2024-02-22 203119](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/fb34a35a-4407-41c0-998e-39bcd12f2337)
![Screenshot 2024-02-22 203125](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/9d576f9d-1f3b-4d1b-b24c-1f85ef597aae)
### viii) RGB and BGR to YCrCb
```
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
### OUTPUT:
![Screenshot 2024-02-22 203145](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/bce2aa2e-a356-4b3a-a83a-9184e9ca60b5)
![Screenshot 2024-02-22 203151](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/5a69445b-0275-49f6-ab7f-62234f1f78dc)
![Screenshot 2024-02-22 203157](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/94dd562c-4d6e-472e-be56-42c2df195189)
### ix) Split and merge RGB Image
```
import cv2
img = cv2.imread('cows.jpg',1)
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
### OUTPUT:
![Screenshot 2024-02-22 203219](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/266fa500-3bed-4f45-9075-4b42f05ee12e)
![Screenshot 2024-02-22 203224](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/072d4f87-59fe-4c4f-a649-ceff9e2443f6)
![Screenshot 2024-02-22 203229](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/6989c627-1fda-42a4-b7de-aa77e52c93de)
![Screenshot 2024-02-22 203235](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/4890fba6-d9c2-4fd2-b2d1-7f46fcf884ff)
### x) Split and merge HSV Image
```
import cv2
img = cv2.imread("cows.jpg",1)
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
### OUTPUT:
![Screenshot 2024-02-22 203259](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/f9c72a8e-3f90-406d-972e-81ba2261a00b)
![Screenshot 2024-02-22 203303](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/bb75b140-2d57-416d-9c83-2f757eb95ccb)
![Screenshot 2024-02-22 203309](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/35ea8de6-b5ed-44b4-bb99-53f8f052cf3a)
![Screenshot 2024-02-22 203316](https://github.com/shabreenavincent/COLOR_CONVERSIONS_OF-IMAGE/assets/119475721/51f8d3a3-8176-48c5-8883-5a7278870859)
## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







