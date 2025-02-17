# Edge-Linking-using-Hough-Transform
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the required modules.

## Step2:
Import the image to operate on.

## Step3:
Convert the imported image from BGR to GRAYSCALE.

## Step4:
Find the edges using canny edge detector and display the image.

## Step5:
Detect the points that form a line using hough transform.

## Step6:
Draw the lines on the image

## Step7:
Display the output

## Step8:
End the program.

## Program:
```
Program to write a Python program to detect the lines using Hough Transform.
Developed by : K.Sucharitha
Ref.no : 212221240021

```Python
# Read image and convert it to grayscale image



import cv2
import matplotlib.pyplot as plt
import numpy as np
image = cv2.imread("suduko.webp")
grayImage = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
plt.imshow(grayImage)
cv2.imshow("Original Image",image)
cv2.imshow("Gray Image",grayImage)


# Find the edges in the image using canny detector and display


import cv2
import matplotlib.pyplot as plt
import numpy as np
image = cv2.imread("ludo.jpg")
grayImage = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
plt.imshow(grayImage,'gray')
cv2.imshow("Original Image",image)
cv2.imshow("Gray Image",grayImage)





# Detect points that form a line using HoughLinesP
lines = cv2.HoughLinesP(cannyEdges,1,np.pi/180,threshold=80,minLineLength = 50,maxLineGap = 250)


# Draw lines on the image
for line in lines:
x1, y1, x2, y2 = line [0]
cv2.line(image,(x1, y1),(x2, y2),(255, 0, 0),3)


# Display the result

plt.title("Hough Transform")
plt.imshow(image,'gray')
plt.show()
```

## Output

### Input image and grayscale image
![output](https://github.com/Sucharithachowdary/Edge-Linking-using-Hough-Transform/blob/main/l%201.jpg?raw=true)
![output](https://github.com/Sucharithachowdary/Edge-Linking-using-Hough-Transform/blob/main/l%202.jpg?raw=true)

### Canny Edge detector output
![output](https://github.com/Sucharithachowdary/Edge-Linking-using-Hough-Transform/blob/main/l%203.jpg?raw=true)

### Display the result of Hough transform
![output](https://github.com/Sucharithachowdary/Edge-Linking-using-Hough-Transform/blob/main/l%204.jpg?raw=true)


## Result:
Thus the program is written with python and OpenCV to detect lines using Hough transform. 
