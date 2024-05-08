# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
<br>
### Step2:
Load the image file in the program.
<br>

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
<br>

### Step4:
Display the modified image output.
<br>

### Step5:
End the program.
<br>

## Program:
```python
Developed By: ADHITHYA PERUMAL D
Register Number: 212222230007
```
```python
i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread( "car.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis( 'off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,100],
               [0,1,100],
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
in_img=cv2.imread("colles.jpeg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```


iii)Image shearing

``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("aaa.jpeg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()

```

iv)Image Reflection
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("bbb.jpeg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  


```


v)Image Rotation


``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("ccc.jpeg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show() 
```

vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("ddd.jpeg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[50:200 ,50:500]
plt.imshow(cropped_img)
plt.show()
```

## Output:

### ORINGINAL IMAGE:
![Screenshot 2024-03-19 125604](https://github.com/DEVADARSHAN2/IMAGE-TRANSFORMATIONS/assets/119432150/20bdee9c-d82e-4c0e-a04a-2e320f1c47f9)

### i)Image Translation
![Screenshot 2024-03-19 125618](https://github.com/DEVADARSHAN2/IMAGE-TRANSFORMATIONS/assets/119432150/742965ed-c75e-4e5f-b7ff-34c6a4b8ef11)



### ii) Image Scaling
![Screenshot 2024-03-19 124859](https://github.com/DEVADARSHAN2/IMAGE-TRANSFORMATIONS/assets/119432150/b32a0356-a4f4-4037-a8df-09603687ffbf)


### iii)Image shearing
![Screenshot 2024-03-19 124929](https://github.com/DEVADARSHAN2/IMAGE-TRANSFORMATIONS/assets/119432150/8310808d-65a7-43f9-ae8c-fc2f7dde6b9d)




### iv)Image Reflection
![Screenshot 2024-03-19 125002](https://github.com/DEVADARSHAN2/IMAGE-TRANSFORMATIONS/assets/119432150/6d568875-2cf2-41cb-a678-e5dfa73ae9f8)


### v)Image Rotation
![Screenshot 2024-03-19 125222](https://github.com/DEVADARSHAN2/IMAGE-TRANSFORMATIONS/assets/119432150/df148516-b2cd-4a02-b333-58d4802f9955)


### vi)Image Cropping
![Screenshot 2024-03-19 125309](https://github.com/DEVADARSHAN2/IMAGE-TRANSFORMATIONS/assets/119432150/9faac685-95b8-4866-9cdc-d08f0ddc20da)





## Result:
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
