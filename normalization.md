#### Batch normalization
##### Algorithm
uses the mean and variance of a mini-batch to normalize each feature channels during training, while in inference phase, BN uses the global statistics to normalize features. The parameters of BN is the scale and shift.

![image](https://github.com/wxiaojie/deep_learning_points/blob/master/images/BN_algorithm.png)

##### advantages:
1. unify the data distribution, more easier to learn so making faster training
2. avoid gradients exploding or vanishing, allowing higher learning rate. ( normalize around 0, so the sigmoid nonlinearity will not satuated)
3. avoid overfitting, the effect similar to dropout as experiments show.

#### Instance normalization
uses the statistics of an individual sample instead of mini-batch to normalize features. Another important difference between IN and BN is that IN applies the same normalize procedure for both training and inference. Instance normalization has been mainly used in the style transfer field. IN can change image appearance while preserving content. Despite these successes, IN has not shown benefits for high-level vision tasks like image classification and semantic segmentation.

Compare BN and IN:
Batch normalization preserves discrimination between individual samples, but also makes CNNs vulnerable to appearance transforms. And
instance normalization eliminates individual contrast, but diminishes useful information at the same time.

#### Layer normalization
However, the effect of batch normalization is dependent
on the mini-batch size and it is not obvious how to apply it to recurrent neural networks.
In this paper, we transpose batch normalization into layer normalization by
computing the mean and variance used for normalization from all of the summed
inputs to the neurons in a layer on a single training case. Like batch normalization,
we also give each neuron its own adaptive bias and gain which are applied after
the normalization but before the non-linearity. Unlike batch normalization, layer
normalization performs exactly the same computation at training and test times.
It is also straightforward to apply to recurrent neural networks by computing the
normalization statistics separately at each time step. Layer normalization is very
effective at stabilizing the hidden state dynamics in recurrent networks. Empirically,
we show that layer normalization can substantially reduce the training time
compared with previously published techniques.

#### group normalization
GN divides the channels into groups and computes within each group the mean and variance for normalization. GN’s computation is independent of batch sizes, and its accuracy is stable in a wide range of batch sizes.

![image](https://github.com/wxiaojie/deep_learning_points/blob/master/images/normalization_method.png)


#### reference:
https://arxiv.org/pdf/1807.09441.pdf
https://arxiv.org/pdf/1607.06450.pdf
https://arxiv.org/pdf/1803.08494.pdf
