# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
### Step2:
Load the image file in the program.
### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
### Step4:
Display the modified image output.
### Step5:
End the program.

## Program:
```python
Developed By: ARVIND S
Register Number: 212222240012
```
i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("porsche.jpeg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,20],
               [0,1,10],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("applehead.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
rows, cols, dims = input_image.shape
M = np.float32([[1.5,0,0],
               [0,1.8,0],
               [0,0,1]])
scaled_image = cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()
```


iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("nature.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
M_x = np.float32([[1,0.5,0],
                 [0,1,0],
                 [0,0,1]])
M_y = np.float32([[1,0,0],
                 [0.5,1,0],
                 [0,0,1]])
shared_image_xaxis = cv2.warpPerspective(input_image,M_x,(int(cols*1.5),int(rows*1.5)))
shared_image_yaxis = cv2.warpPerspective(input_image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(shared_image_xaxis)
plt.show()
plt.axis('off')
plt.imshow(shared_image_yaxis)
plt.show()
```
iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("space.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
rows,cols,dim = input_image.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x = cv2.warpPerspective(input_image,M_x,(int(cols),int(rows)))
reflect_y = cv2.warpPerspective(input_image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()
```

v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("tiger.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
rows,cols,dim = input_image.shape
angle = np.radians(10)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img = cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show() 
```

vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("spyder.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.imshow(input_image)
plt.show()
cropped_img=input_image[50:200 ,50:500]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### Original Image
![Screenshot 2024-03-08 184255](https://github.com/S-ARVIND01/IMAGE-TRANSFORMATIONS/assets/118707337/b38cc2d9-6992-4558-b5dd-c24ab6c934d7)

### i)Image Translation
![Screenshot 2024-03-08 200302](https://github.com/S-ARVIND01/IMAGE-TRANSFORMATIONS/assets/118707337/3f0487aa-07a5-4e87-919f-af26a96e665a)

### ii) Image Scaling
![Screenshot 2024-03-08 182722](https://github.com/S-ARVIND01/IMAGE-TRANSFORMATIONS/assets/118707337/5b1b47eb-6258-4045-bbc4-2ca869406c9f)

### iii)Image shearing
![Screenshot 2024-03-08 184819](https://github.com/S-ARVIND01/IMAGE-TRANSFORMATIONS/assets/118707337/5e935ab1-5799-4ad2-a9ec-0b2b72eae43b)
![Screenshot 2024-03-08 184831](https://github.com/S-ARVIND01/IMAGE-TRANSFORMATIONS/assets/118707337/7d74f897-d0f2-40f7-9e37-4a9596914b54)

### iv)Image Reflection
![Screenshot 2024-03-08 184845](https://github.com/S-ARVIND01/IMAGE-TRANSFORMATIONS/assets/118707337/45950963-3bf1-4343-8d49-1a7dd768791c)
![Screenshot 2024-03-08 184903](https://github.com/S-ARVIND01/IMAGE-TRANSFORMATIONS/assets/118707337/13305b73-af69-4a22-8087-9c6ab11184d4)

### v)Image Rotation
![Screenshot 2024-03-08 182925](https://github.com/S-ARVIND01/IMAGE-TRANSFORMATIONS/assets/118707337/d56569ec-c3e5-4e57-8ff0-58c0d28b0a5e)

### vi)Image Cropping
![Screenshot 2024-03-08 184918](https://github.com/S-ARVIND01/IMAGE-TRANSFORMATIONS/assets/118707337/60de7a30-7ee6-4202-921e-a160fd9ed729)
![Screenshot 2024-03-08 184931](https://github.com/S-ARVIND01/IMAGE-TRANSFORMATIONS/assets/118707337/f5760423-6de3-493c-86f8-9083ccb5bd05)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
