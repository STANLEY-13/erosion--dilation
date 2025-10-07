# Implementation-of-Erosion-and-Dilation
# Aim
To implement Erosion and Dilation using Python and OpenCV.

# Software Required

Anaconda - Python 3.7
OpenCV

# Algorithm:
### Step1:
import the neccesary packages

### Step2:
create the text using cv2.put Text

### Step3:
create the structuting element

### Step4:
Erodde the image

### Step5:
Dilate the image

# Program:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
## Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
## Add text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Vinnusheh', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
## Display the input image
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
## Create a simple square kernel (3x3)
```
kernel = np.ones((3, 3), np.uint8)
```
## Apply erosion (shrinking effect)
```
eroded_image = cv2.erode(image, kernel, iterations=1)
```
## Display the eroded image
```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```
# Output:

### Display the input Image
<img width="491" height="520" alt="image" src="https://github.com/user-attachments/assets/1fa803b5-48d2-4905-acbb-c897ad624565" />


### Display the Eroded Image
<img width="512" height="510" alt="image" src="https://github.com/user-attachments/assets/1eaa4f78-e456-4c0d-a230-48256e85f0a7" />


### Display the Dilated Image
<img width="498" height="527" alt="image" src="https://github.com/user-attachments/assets/4b179d00-ffbd-42e2-af01-a16250b169dc" />


# Result
Thus the generated text image is eroded and dilated using python and OpenCV.
