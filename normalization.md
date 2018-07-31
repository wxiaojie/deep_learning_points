1. Batch normalization : uses the mean
and variance of a mini-batch to normalize each feature channels during training,
while in inference phase, BN uses the global statistics to normalize features.

2. Instance normalization: uses the statistics
of an individual sample instead of mini-batch to normalize features. Another important
difference between IN and BN is that IN applies the same normalize procedure
for both training and inference. Instance normalization has been mainly
used in the style transfer field. IN can change image appearance
while preserving content. Despite these successes, IN has not shown benefits
for high-level vision tasks like image classification and semantic segmentation.

Compare BN and IN:
Batch normalization preserves discrimination between individual
samples, but also makes CNNs vulnerable to appearance transforms. And
instance normalization eliminates individual contrast, but diminishes useful information
at the same time.


### reference:

https://arxiv.org/pdf/1807.09441.pdf
