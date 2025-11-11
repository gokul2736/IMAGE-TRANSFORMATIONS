# IMAGE-TRANSFORMATIONS

# Name: Markandeyan Gokul
# Reg: 212224240086

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import the necessary libraries and read the original image and save it as a image variable.

### Step2:

Translate the image using a function warpPerpective()

### Step3:

Scale the image by multiplying the rows and columns with a float value.

### Step4:

Shear the image in both the rows and columns.

### Step5:

Find the reflection of the image.

### Step6:

Rotate the image using angle function.
## Program:
```
Developed By: Bharathganesh S
Register Number: 212222230022
```
```
i)Image Translation
import cv2
import numpy as np

# Load the image
image = cv2.imread('cat.jpg')

# Define translation matrix: (shift along x, shift along y)
tx, ty = 100, 50
translation_matrix = np.float32([[1, 0, tx], [0, 1, ty]])

# Apply translation
translated_image = cv2.warpAffine(image, translation_matrix, (image.shape[1], image.shape[0]))

# Display
cv2.imshow('Translated Image', translated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

ii) Image Scaling
# Scaling factors
scale_x, scale_y = 1.5, 1.5

# Resize image
scaled_image = cv2.resize(image, None, fx=scale_x, fy=scale_y, interpolation=cv2.INTER_LINEAR)

# Display
cv2.imshow('Scaled Image', scaled_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

iii)Image shearing
# Define shearing matrix
shear_factor = 0.5
shearing_matrix = np.float32([[1, shear_factor, 0], [0, 1, 0]])

# Apply shearing
sheared_image = cv2.warpAffine(image, shearing_matrix, (int(image.shape[1] * 1.5), image.shape[0]))

# Display
cv2.imshow('Sheared Image', sheared_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

iv)Image Reflection
 Reflection_Image= cv2.flip(image, 1)

# Display
cv2.imshow('Reflection Image', Reflection_Image)
cv2.waitKey(0)
cv2.destroyAllWindows()

v)Image Rotation
# Rotation center, angle and scale
center = (image.shape[1] // 2, image.shape[0] // 2)
angle, scale = 45, 1.0

# Get rotation matrix
rotation_matrix = cv2.getRotationMatrix2D(center, angle, scale)

# Apply rotation
rotated_image = cv2.warpAffine(image, rotation_matrix, (image.shape[1], image.shape[0]))

# Display
cv2.imshow('Rotated Image', rotated_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

vi)Image Cropping
# Define the region of interest (ROI)
x, y, w, h = 100, 100, 300, 300
cropped_image = image[y:y+h, x:x+w]

# Display
cv2.imshow('Cropped Image', cropped_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:

## Original image

![image](https://github.com/user-attachments/assets/da97cc21-ee27-4541-8db5-0bdd5df99eec)

### i)Image Translation

![image](https://github.com/user-attachments/assets/d10ceccf-24d2-4818-9d5d-9b870c9e35df)


### ii) Image Scaling

![image](https://github.com/user-attachments/assets/3ebcea28-9d82-4568-bb8d-18afcbdd088e)


### iii)Image shearing
![image](https://github.com/user-attachments/assets/61a75e75-7830-446d-902d-ccde8e645862)

![image](https://github.com/user-attachments/assets/c8d1d66d-9d67-48e0-84c6-d7e3a983b225)

### iv)Image Reflection

![image](https://github.com/user-attachments/assets/9e1e0f48-2566-4cbb-ad51-ce55d8a3e60b)

![image](https://github.com/user-attachments/assets/2b561dd9-9aac-4b1c-a531-fe2448868c4c)


### v)Image Rotation
![image](https://github.com/user-attachments/assets/01a8c573-4462-46d7-b39c-5f47486b90e6)




### vi)Image Cropping
![image](https://github.com/user-attachments/assets/27ad0f61-d896-4ba2-98d5-76490fe8fe1e)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
