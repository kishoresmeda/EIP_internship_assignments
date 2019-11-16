# MNSIT-image-classifier

Test score - 0.9921

Understanding of the below terminologies
1. Convolution - A process of applying a matrix on an image usually of size 3x3 and sliding it across the whole image to get a matrix.
2. Filters/Kernels - A matrix of size 3x3 used to extract specific features in an image.
3. Epochs - Number of times the model has been trained with the complete dataset. 10 epochs mean the model has been trained with the complete data 10 times.
4. 1x1 Convolution - A filter used of size 1x1 will convolve 1 pixel of an image at a given time.
5. 3x3 Convolution - A filter used of size 3x3 will convolve 9 pixels at a time and takes less number of strides compared to the 1x1 convolution.
6. Feature Maps - When a filter containing a specific feature is used on the whole image, the resultant matrix will contain all the instances of that feature in the image. An edge feature map will have all the edges in an image.
7. Activation function - Function used to remove linearity in the signal.
8. Receptive field - A region in an image which is the neural network is looking at for a particular feature.
