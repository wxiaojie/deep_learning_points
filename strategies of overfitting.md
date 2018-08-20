#### Network Architecture

1. Dropout is proposed by Hinton et al. [5] as a regularizer which randomly sets half of the activations 
to the fully connected layers to zero during training.  ---- reduce sample noise
It has improved the generalization ability and largely prevents overfitting. (from paper NIN)

2. Global average pooling has no parameter, so it can avoid overfitting compared to fully connected layers.

3. L2 normalization (weight decay)

4. Batch normalization---- reduce sample noise

layer normalization ----  "When image appearances are
presented, simple appearance variations such as color or brightness shift could
simply be eliminated by normalizing each RGB channel of an image with its
mean and standard deviation" ----- https://arxiv.org/pdf/1807.09441.pdf

instance normalization -- appearance invariance (domain generalization) ----  hidden layer

5. increase the invariance: max pooling, deformable convolution(kernel learns the connection way, not the fixed position, finally the learned kernel will connected to meaningful pixels)

#### others

6. transfer learning: initialize the weights of the CNN to eg. ImageNet pretrained model  [some discussion in paper: Show and Tell]

7. ensemble --- trade-off stochastics

#### Data
data augmentation: translation （random crop), horizontal flipping.
