# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result

## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
image = np.zeros((500, 500, 3), dtype=np.uint8)
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'PAVITHRAN MJ', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create the structuring element
kernel = np.ones((3, 3), np.uint8)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input image with text")
plt.axis('off')


# Use Opening operation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')


# Use Closing Operation
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)

```
## Output:

### Display the input Image
<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/8dc0ff8c-eaac-48f5-bf55-0d3448b1def7" />



### Display the result of Opening

<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/aba95eff-8492-48dc-a4db-545e0412114a" />


### Display the result of Closing

<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/8dc0ff8c-eaac-48f5-bf55-0d3448b1def7" />


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
