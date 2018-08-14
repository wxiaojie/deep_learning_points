### Relu
relu = max(x, 0), 
where x=0 is not differentiable, which is set as 0. 

Thus the derivative of relu is 1 where x > 0 and 0 where x <=0.

### pooling
pooling changes the size of feature map, for 64 gradients --- 2*2 pooling ---- 
16 gradients. Thus the gradient of one pixel should be allocated to 4 pixels of 
the last layer to maintain the sum of the loss unchanged.
1. mean pooling
average the gradient

2. max pooling
assign the gradient to the pixel with max value of the last layer, and other pixels
are without gradient.
