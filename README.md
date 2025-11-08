# EXP-9
# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:

Create the structuring element.
### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program
# Import the necessary packages
```
Developed by : Aswin.L
Reg no : 212224230028

import cv2
import numpy as np
import matplotlib.pyplot as plt
```


# Create the Text using cv2.putText
```
img = np.zeros((100, 550), dtype = 'uint8')
font = cv2.FONT_ITALIC
cv2.putText(img, 'Ayisha Rinsi K', (5,70), font, 2, (255), 5, cv2.LINE_AA)
n_img = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(n_img)
plt.axis("off")
```


# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (11,11) )
```
# Use Opening operation
```
image_open = cv2.morphologyEx(n_img, cv2.MORPH_OPEN, kernel)
plt.imshow(image_open)
plt.axis("off")

```
# Use Closing Operation
```
image_close = cv2.morphologyEx(n_img, cv2.MORPH_CLOSE, kernel)
plt.imshow(image_close)
plt.axis("off")



```
## Output:

### Display the input Image
<img width="730" height="134" alt="Screenshot 2025-11-08 110812" src="https://github.com/user-attachments/assets/4746b3b4-23d1-43fe-a1d8-f4e923750923" />



### Display the result of Opening
<img width="584" height="124" alt="Screenshot 2025-11-08 111118" src="https://github.com/user-attachments/assets/ed8fe170-3074-4715-a56f-9830b780d297" />



### Display the result of Closing
<img width="734" height="145" alt="Screenshot 2025-11-08 110831" src="https://github.com/user-attachments/assets/5504b18b-fc84-4797-b5d5-5f200cf62230" />



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
