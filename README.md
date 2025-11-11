# IMAGE-TRANSFORMATIONS

# Name: Markandeyan Gokul
# Reg: 212224240086

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1:

Import all the necessary modules

### Step2:

Choose an image and save it as filename.jpg
### Step3:


Use imread to read the image
### Step4:
Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image
### Step5:
Use cv2.warpPerspective(image,M,(cols*2,rows*2)) to scale the image
### Step6:
Use cv2.warpPerspective(image,M,(int(cols*1.5),int(rows*1.5))) for x and y axis to shear the image
### Step7:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image
### Step8:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image
### Step9:
Crop the image to remove unwanted areas from an image
### Step10:

Use cv2.imshow to show the image
### Step11:
<br>
End the program

## Program:

### Original image 
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread('dogs.jpeg')
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(image)
plt.show()
```
## OUPUT :
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/e258159b-cf6f-4c56-9a62-22f39ad47ecc)

### i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dogs.jpeg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[1,0,114],[0,1,-230],[0,0,1]])
translated_image = cv2.warpPerspective(image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
## OUPUT :
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/30651e12-b8a4-4dd2-9cc9-3cd4a900b3fc)

### ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dogs.jpeg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[2.4,0 ,0],[0,1.9,0],[0,0,1]])
scaled_image = cv2.warpPerspective(image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()
```
## OUPUT :
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/9b0bee0f-f070-4c1c-993f-64001fdb22b6)

### iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dogs.jpeg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0.8 ,0],[0,1,0],[0,0,1]])
M_y = np.float32([[1,0,0],[0.6,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.imshow(sheared_img_yaxis)
plt.show()
```
## OUTPUT :
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/7a2831ff-c2d3-4b28-be2b-d218247ff2ab)

### iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dogs.jpeg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0 ,0],[0,-1,rows],[0,0,1]])
M_y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.imshow(reflected_img_yaxis)
plt.show()
```
## OUPUT :

<img width="319" alt="image" src="https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/f5695a57-86f5-4de2-802e-266ab6ce3789">

### v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dogs.jpeg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
angle = np.radians(10)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
## OUPUT :
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/312d2c70-6cca-4f31-a0db-2ebd67a2fd49)


### vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dogs.jpeg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
cropped_img = image[100:800,20:400]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## OUPUT :
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/9c57bae7-d560-443b-ba55-ad821dc93206)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
