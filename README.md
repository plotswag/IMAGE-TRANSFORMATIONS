# EX 4
# IMAGE-TRANSFORMATIONS
## DATE:
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
Developed By: Jeevanesh
Register Number: 212222243002
```

## i)Image Translation

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("kamal2.jpg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

## ii) Image Scaling

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("kamal2.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```


## iii)Image shearing

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("kamal2.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```


### iv)Image Reflection

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("kamal2.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```


### v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("kamal2.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()

angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(input_image,M,(int(cols),int(rows)))

plt.imshow(rotated_img)
plt.show()
```



### vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("kamal2.jpg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```


## Output:
### i)Image Translation

![Screenshot 2024-11-18 214026](https://github.com/user-attachments/assets/bcb14da2-091a-40b9-91ab-c58ff66ec4eb)


### ii) Image Scaling

![Screenshot 2024-11-18 214037](https://github.com/user-attachments/assets/eb49646b-9d30-4aa2-bb95-9b7dcfd8de98)



### iii)Image shearing

![Screenshot 2024-11-18 214046](https://github.com/user-attachments/assets/1435d8f2-d724-465c-8a9a-7a8d2e9fdfe2)

![Screenshot 2024-11-18 214059](https://github.com/user-attachments/assets/f81687d3-87d0-4662-a411-ef6de67670ef)


### iv)Image Reflection

![Screenshot 2024-11-18 214111](https://github.com/user-attachments/assets/71451076-d0ab-4e59-8519-4f60c93228e4)


![Screenshot 2024-11-18 214118](https://github.com/user-attachments/assets/09e74ea5-57f2-4524-918a-f237674d0341)


### v)Image Rotation

![Screenshot 2024-11-18 214125](https://github.com/user-attachments/assets/8ce61514-a170-4df6-84f6-a3c37145d29b)




### vi)Image Cropping
![Screenshot 2024-11-18 214132](https://github.com/user-attachments/assets/713c3ce0-26f8-41cf-be59-eca884439139)



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
