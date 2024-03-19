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
Developed By: HARISH G
Register Number: 212222243001
```
i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("car_1.jpg")
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
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("car_2.jpeg")
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
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("car_3.jpeg")
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
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("car_4.jpeg")
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
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("car_5.jpg")
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
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("car_6.jpeg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.imshow(input_image)
plt.show()
cropped_img=input_image[100:500 ,200:1000]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### Original Image
![Screenshot 2024-03-19 202558](https://github.com/Harish2404lll/IMAGE-TRANSFORMATIONS/assets/141472096/f70097b6-ba85-44d3-9e50-bb7c30dbc913)

### i)Image Translation
![Screenshot 2024-03-19 202621](https://github.com/Harish2404lll/IMAGE-TRANSFORMATIONS/assets/141472096/d08b18d4-69cc-4a4b-a899-c38fa542f1a6)

### ii) Image Scaling
![Screenshot 2024-03-19 202633](https://github.com/Harish2404lll/IMAGE-TRANSFORMATIONS/assets/141472096/423beee0-a421-4a44-928c-7eb33c98cbea)

### iii)Image shearing
![Screenshot 2024-03-19 202703](https://github.com/Harish2404lll/IMAGE-TRANSFORMATIONS/assets/141472096/bdeb9266-6e70-4ce7-84bd-6b6e423db373)

### iv)Image Reflection
![Screenshot 2024-03-19 202724](https://github.com/Harish2404lll/IMAGE-TRANSFORMATIONS/assets/141472096/3b6899ad-3b28-47d6-82b6-9ccc0166d756)
![Screenshot 2024-03-19 202754](https://github.com/Harish2404lll/IMAGE-TRANSFORMATIONS/assets/141472096/b17b2c7f-43e5-4a60-8d29-5f33bfafc4a8)

### v)Image Rotation
![Screenshot 2024-03-19 202840](https://github.com/Harish2404lll/IMAGE-TRANSFORMATIONS/assets/141472096/09ada959-bda7-4b27-b952-d1df3d411dd8)

### vi)Image Cropping
![Screenshot 2024-03-19 203552](https://github.com/Harish2404lll/IMAGE-TRANSFORMATIONS/assets/141472096/0a9c4dec-c7fc-4073-8164-c6028bfdd5e8)
![Screenshot 2024-03-19 203600](https://github.com/Harish2404lll/IMAGE-TRANSFORMATIONS/assets/141472096/767e4b0e-1116-493c-98c2-fdd8d50175c1)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
