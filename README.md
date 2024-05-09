# Exp:09 Implementation of Erosion and Dilation

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
developed by: Praveen.v
reg no:212222233004

```
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Downloads/photo.png',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')


# Create the structuring element
# Create the structuring element
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)


# Erode the image
# Erode the image
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')


# Dilate the image
# Dilate the image
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')


```
## Output:

### Display the input Image
![exp 9](https://github.com/praveenv23013808/erosion--dilation/assets/145824728/bf846d78-4156-4285-85ae-3926fddcc166)

# Create the structuring element

![Screenshot 2024-05-09 075533](https://github.com/praveenv23013808/erosion--dilation/assets/145824728/8d08487d-da90-4f84-a02e-95363fdefff4)


### Display the Eroded Image

![Screenshot 2024-05-09 075558](https://github.com/praveenv23013808/erosion--dilation/assets/145824728/f3188842-6b3f-4478-b9ff-8cbc30c9632a)

### Display the Dilated Image
![Screenshot 2024-05-09 075626](https://github.com/praveenv23013808/erosion--dilation/assets/145824728/88a2062f-c88e-4085-be5e-ba77bb7f6aae)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
