# FER
INTRODUCTION 
			Emotions are exhibited through facial expressions that are consistently correspondent. This means that regardless of language and cultural barriers, there will
			always be a set of fundamental facial expressions that people assess and communicate with. After extensive research,it is now generally agreed that humans share 
			seven facial expressions that reflect the experiencing of fundamental emotions. These fundamental emotions are anger, disgust, fear, happiness, sadness, surprise 
			and neutral. Facial Expression Recognition (FER) datasets are utilized below are obtained from kaggle. Lets take a look at the brief explanation of some of the 
			techniques used to improve our model performance and reduce the training time.
Regularization is a technique which makes slight modifications to the learning algorithm such that the model generalizes better. This in turn improves the model’s 
      performance on the unseen data as well.
Data normalization: We can normalize the image tensors by subtracting the mean and dividing by the standard deviation of pixels across each channel. Normalizing the
      data prevents the pixel values from any one channel from disproportionately affecting the losses and gradients. Learn more
Data augmentation: We can apply random transformations while loading images from the training dataset. Specifically, we will pad each image by 4 pixels, and then take a 
      random crop of size 32 x 32 pixels, and then flip the image horizontally with a 50% probability. Learn more
Residual connections: Addition of the residual block adds the original input back to the output feature map obtained by passing the input through one or more 
      convolutional layers. We use the ResNet9 architecture Learn more.
Batch normalization: After each convolutional layer, we add a batch normalization layer, which normalizes the outputs of the previous layer. This is somewhat similar to 
      data normalization, except it’s applied to the outputs of a layer, and the mean and standard deviation are learned parameters. Learn more
Learning rate scheduling: Instead of using a fixed learning rate, we can use a learning rate scheduler, which will change the learning rate after every batch of training.
      There are many strategies for varying the learning rate during training, and we used the “One Cycle Learning Rate Policy”. Learn more.
Weight Decay: We add weight decay to the optimizer, yet another regularization technique which prevents the weights from becoming too large by adding an additional term
      to the loss function. Learn more
Gradient clipping: We also add gradient clipping, which helps limit the values of gradients to a small range to prevent undesirable changes in model parameters due to 
      large gradient values during training. Learn more.
Adam optimizer: We use the Adam optimizer which uses techniques like momentum and adaptive learning rates for faster training. There are many other optimizers to choose 
      from a and experiment with. Learn more.
SOURCE OF DATA
     We make use of Facial expression dataset image folders (fer2013) in kaggle to implement this model. Data is divided into training (80%), testing (10%), and
		 validation(10%) sets in ImageFolder format. 
Do check out my blog for more details: https://medium.com/@afram.p245/emotion-detection-through-facial-feature-recognition-a1c1a7a38c23
