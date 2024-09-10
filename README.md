# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
	Draw a line from the top-left to the bottom-right of the image.
	Draw a circle at the center of the image.
	Draw a rectangle around a specific region of interest in the image.
	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
	Convert the image from RGB to HSV and display it.
	Convert the image from RGB to GRAY and display it.
	Convert the image from RGB to YCrCb and display it.
	Convert the HSV image back to RGB and display it.

### Step4:
	Access and print the value of the pixel at coordinates (100, 100).
	Modify the color of the pixel at (200, 200) to white.

### Step5:
	Resize the original image to half its size and display it.
### Step6:
	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
	Flip the original image horizontally and display it.
	Flip the original image vertically and display it.
### Step8:
	Save the final modified image to your local directory.
```
Developed By: THRIKESHWAR P
Register Number: 212222230162
```
# Program:

### 1)Read and Display an Image

```Python
import cv2
image=cv2.imread('loki.jpg')
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
 

### OUTPUT:
![image](https://github.com/user-attachments/assets/9a748896-3312-4158-988c-69ec5d0863e4)



 

### 2.) Draw Shapes and Add Text:
i)Draw a line from the top-left to the bottom-right of the image.

```Python
import cv2
img = cv2.imread('loki.jpg')
img=cv2.resize(img,(600,800))
res = cv2.line(img, (0, 0), (599, 799), (200, 100, 205), 10)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>


### OUTPUT:

![image](https://github.com/user-attachments/assets/714ecd35-f4f8-41bd-82aa-facccf745985)



 
### ii)Draw Shapes and Add Text
```Python
import cv2


img = cv2.imread('loki.jpg')
img1=cv2.resize(img,(600,800))


height, width, _ = img1.shape


center_coordinates = (width // 2, height // 2)


res = cv2.circle(img1, center_coordinates, 150, (255, 0, 0), 10)

cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>


### OUTPUT:
![image](https://github.com/user-attachments/assets/ed3dd469-3fa9-4ed6-924c-4589983bc904)




      
### iii)Draw a rectangle around a specific region of interest in the image.
```Python

import cv2
img = cv2.imread('loki.jpg')
img1=cv2.resize(img,(600,800))
start=(0,0)
stop=(409,529)
color=(100,255,100)
thickness=10
res_img=cv2.rectangle(img1,start,stop,color,thickness)

cv2.imshow('Image Window', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
 <br>
 <br>

### OUTPUT:

![image](https://github.com/user-attachments/assets/ea326960-52b7-48a4-be16-6d38042930e6)




      
### iv)Add the text "OpenCV Drawing" at the top-left corner of the image.

 ```Python
import cv2

img = cv2.imread('loki.jpg')
img1=cv2.resize(img,(600,800))

text = "OPENCV DRAWING"
position = (50, 50)  # Positioning the text at the top-left corner

font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255)  # White color
thickness = 2


res = cv2.putText(img1, text, position, font, font_scale, color, thickness, cv2.LINE_AA)


cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()


```
<br>
<br>

    
### OUTPUT:

![image](https://github.com/user-attachments/assets/12c97714-69a5-4c84-bf61-3a81ef103a50)




### 3)Image Color Conversion
i)Convert the image from RGB to HSV and display it.
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### OUTPUT:
![image](https://github.com/user-attachments/assets/2be562c3-dc96-4a8c-98c0-b905a9af4395)


#### ii.)Convert the image from RGB to GRAY and display it.
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output:
![image](https://github.com/user-attachments/assets/4815f911-9a52-4e0d-864a-6b90aeb7648c)



#### iii.)Convert the image from RGB to YCrCb and display it.
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Output:
![image](https://github.com/user-attachments/assets/b766b99d-c120-4f1f-9398-a776e2171208)


#### iv.)Convert the HSV image back to RGB and display it.
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/c176ac07-7242-435c-962c-663064b4cbe6)


## 4. Access and Manipulate Image Pixels:
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img, (300, 200))
cv2.imshow('Original Image', img)
pixel_value = img[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
img[199, 199] = [255, 255, 255]
cv2.imshow('Modified Image', img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/f7c2bd0f-8ae9-49da-aef6-1f3cf13cd726)


## 5. Image Resizing:
```Python
import cv2
img = cv2.imread('loki.jpg')
width=600
height=800
half_width=300
half_height=400
resized_img = cv2.resize(img, (300, 400))
cv2.imshow('Original',image)
cv2.imshow('resized',resized_img)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/a3184179-9652-4cd8-ad63-1b0492f761c7)


## 6.Image Cropping:
```Python
import cv2
img = cv2.imread('loki.jpg')
img1=cv2.resize(image1,(600,800))
x, y = 50, 50
width, height = 100, 100
roi = image1[y:y + height, x:x + width]
cv2.imshow('Cropped Image', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/ac6cc533-f6f8-494e-9105-612fb0cd9771)




## 7.Image Flipping:
i.)Flip the original image horizontally and display it.
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
res=cv2.rotate(img,cv2.ROTATE_180)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/389e723c-ff7d-4ec9-978c-acfda4988471)




#### ii.)Flip the original image vertically and display it.

```Python
import cv2
img = cv2.imread('loki.jpg')
img1=cv2.resize(img,(600,800))
img = cv2.resize(img1,(300,200))
res=cv2.rotate(img,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('Original',img)
cv2.imshow('Image Window', res)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/beceefbe-80be-4086-96fc-4e5d9624ba17)



## 8. Write and Save the Modified Image:
```Python
import cv2
img = cv2.imread('loki.jpg')
img = cv2.resize(img,(300,200))
cv2.imwrite('lokesh1.jpg',img)
```
<br>
<br>

### Output:
![image](https://github.com/user-attachments/assets/71c295e8-d538-41a2-b9cb-31a72df4b395)



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







