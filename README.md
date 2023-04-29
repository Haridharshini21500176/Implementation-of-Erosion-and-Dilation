# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>
Import the necessary packages.

### Step2:
<br>
Create the text image using cv2.putText.

### Step3:
<br>
Then create the structuring image for dilation/erosion.

### Step4:
<br>
Apply erosion and dilation using cv2.erode and cv2.dilate.

### Step5:
<br>
Plot the images using plt.imshow.
 
## Program:
```
Developed by:HARIDHARSHINI.S
Reg_No:212221230033
```

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
text_image = np.zeros((100,550),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image,"S.HARIDHARSHINI",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
image_erode = cv2.erode(text_image,kernel)
plt.title("Eroded Image")
plt.imshow(image_erode,'magma')
plt.axis('off')

# Dilate the image
image_dilate = cv2.dilate(text_image,kernel)
plt.title("Dilated Image")
plt.imshow(image_dilate,'magma')
plt.axis('off')

```
## Output:

### Display the input Image
![10 1](https://user-images.githubusercontent.com/94168395/235294036-35b47222-a32c-41aa-81e0-c8119fda4969.png)
<br>

### Display the Eroded Image
![10 2](https://user-images.githubusercontent.com/94168395/235294042-d89b4da6-36b6-412f-a474-7446b9e1c9ff.png)
<br>

### Display the Dilated Image
![10 3](https://user-images.githubusercontent.com/94168395/235294048-ca612eec-5c22-4191-a6e3-5b05ec2d0da9.png)
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
