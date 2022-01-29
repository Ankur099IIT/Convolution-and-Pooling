# Convolution-and-Pooling


we have used the 3D image having shape(634,525,3).
#Since we want to use the image without RGB so we have to change the shape of the image to 2D (634, 525)

we also resized the image.

for ex: suppose we have 5 by 5 input image then we apply 3 by 3 filter on it and then convolute, we will be having 3 by 3 output/transformed image and each values/pixel value of the transformed image matrix is the convolution that we are calculating here.

In Pooling, the step size is 2 because we are using 2 by 2 pooling

x and y are divided by 2 in new_image because we are defining the position of the integer value of the max pixel in the new image which should be like 0,1,2,…. But our steps in for loop are 0,2,4,6…..)


#Concept of Convolution and Pooling

Computer Vision-

Image classification- identify the image

Object detection- identify the image as well as the location (for ex: self -driven car application, identifying the car and also its position in the road)

Edge detection- 
•	vertical edge detection
•	horizontal edge detection

•	Vertical edge detection-

Suppose we have 6 by 6 matrix (assuming 6 pixels by 6 pixels grey image), then we define a filter/kernel (let us suppose 3 by 3 matrix) and then convolute it through our 6 by 6 matrix so we come up with 4 by 4 matrix and the values in this matrix will be calculated by element by element multiplication and sum them up. This is known as convolution operation. 


		 


0-255

0-	Darker colour, 255- brighter colour
 

The vertical edge detection filter will be having lighter pixels (higher number) in the left of the matrix and lower number or darker pixels on the right of the matrix. So as to create a lighter middle region after convolution to detect vertical edges in an image  efficiently.


•	Horizontal edge detection- flip vertical filter by 90 degrees

 

Values/weights in the filter matrix can also be found by treating them as a features which creates more robust edge detection mechanism fo our particular problem.

Padding-

Issue with convolution operation is 
•	Considers Less information of pixels at the edges (through away information at edges)
•	Reduces the size of matrix after each convolution (shrinky output)

This problem can be removed by using padding- which is adding an extra layer of pixel at the boundary (padding can be of 1 pixel, 2 pixel etc.)


Valid convolution- no padding used

Same convolution- padding is used in such a way that output matrix (line detected in it) will have the same dimensions as that of the input image matrix.

Note- common computer vision convention, the filter dimensions are usually odd (forex: 3 by 3, 5 by 5 etc)


Strided convolution-

Stride=2 means we convolute our filter on to the input matrix by jumping two rows and two columns resulting in much smaller dimension output matrix.




Pooling- In pooling, suppose we have 4 by 4 input image then we divide the image in equal part of 4 and calculate the maximum value (intuition of high chances to capture feature) in each quadrant. This is similar to apply 2 by 2 filter with stride=2.

Max pooling is a type of pooling.
Note- when we use pooling, usually we do not use padding

 



