UNet is a fully convolutional neural network that is designed to learn better from fewer training samples.
![image](https://user-images.githubusercontent.com/94308793/200098372-547932f9-535f-4b2c-87f6-c88dc9569f0c.png)
UNET  is a U-shaped encoder-decoder network architecture, which consists of four encoder blocks and four decoder blocks that are connected via a bridge.

The encoder network acts as the feature extractor and learns an abstract representation of the input image through a sequence of the encoder blocks. Each encoder block consists of two 3×3 convolutions, where each convolution is followed by a ReLU (Rectified Linear Unit) activation function. The output of the ReLU acts as a skip connection for the corresponding decoder block. These skip connections provide additional information that helps the decoder to generate better semantic features.

The bridge connects the encoder and the decoder network and completes the flow of information.

The decoder network is used to take the abstract representation and generate a semantic segmentation mask. The output of the last decoder passes through a 1×1 convolution with sigmoid activation. The sigmoid activation function gives the segmentation mask representing the pixel-wise classification.
<br><br><br>
I was able to complete the first epoch before Colab crashed:
![image](https://user-images.githubusercontent.com/94308793/200098534-9d2adb28-97c2-4599-b53d-408f9a855db4.png)
The results obtained show that the accuracy is 0.5078 and the jacard_coef is 0.1820.

Furthermore, you can see some of the example cases:
![image](https://user-images.githubusercontent.com/94308793/200098619-98fb100d-21c8-4e95-9c3c-6694bd1fb7df.png)
![image](https://user-images.githubusercontent.com/94308793/200098633-36baa93a-242f-4c1e-be47-b21cff27102a.png)
