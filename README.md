# Convolution-and-Pooling


we have used the 3D image having shape(634,525,3).
#Since we want to use the image without RGB so we have to change the shape of the image to 2D (634, 525)

we also resized the image.

for ex: suppose we have 5 by 5 input image then we apply 3 by 3 filter on it and then convolute, we will be having 3 by 3 output/transformed image and each values/pixel value of the transformed image matrix is the convolution that we are calculating here.

In Pooling, the step size is 2 because we are using 2 by 2 pooling

x and y are divided by 2 in new_image because we are defining the position of the integer value of the max pixel in the new image which should be like 0,1,2,…. But our steps in for loop are 0,2,4,6…..)
