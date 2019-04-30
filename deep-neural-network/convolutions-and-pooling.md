# Convolutions and Pooling

### Convolution

usually involves having a filter and passing that filter over the image in order to change the underlying image. The process works a little bit like this. For every pixel, take its value, and take a look at the value of its neighbors. If our filter is three by three, then we can take a look at the immediate neighbor, so that you have a corresponding three by three grid. Then to get the new value for the pixel, we simply multiply each neighbor by the corresponding value in the filter. So, for example, in this case, our pixel has the value 192, and its upper left neighbor has the value zero. The upper left value and the filter is negative one, so we multiply zero by negative one. Then we would do the same for the upper neighbor. Its value is 64 and the corresponding filter value was zero, so we'd multiply those out. Repeat this for each neighbor and each corresponding filter value, and would then have the new pixel with the sum of each of the neighbor values multiplied by the corresponding filter value, and that's a convolution



{% hint style="info" %}
ConvNets only capture local “spatial” patterns in data. If the data can’t be made to look like an image, ConvNets are less useful.
{% endhint %}

### Rule of thumb

{% hint style="warning" %}
If your data is just as useful after swapping any of your columns with each other, then you can’t use Convolutional Neural Networks. \(like customer data, if you move columns around, the meaning of the data does not change. On the other hand, with an image if you move pixels around, the image is no longer the same image\)
{% endhint %}

{% hint style="warning" %}
ConvNets are great at finding patterns and using them to classify images.
{% endhint %}



![](../.gitbook/assets/image%20%2831%29.png)

### Pooling

But simply, pooling is a way of compressing an image. A quick and easy way to do this, is to go over the image of four pixels at a time, i.e, the current pixel and its neighbors underneath and to the right of it. Of these four, pick the biggest value and keep just that. So, for example, you can see it here. My 16 pixels on the left are turned into the four pixels on the right, by looking at them in two-by-two grids and picking the biggest value. This will preserve the features that were highlighted by the convolution, while simultaneously quartering the size of the image. We have the horizontal and vertical axes.

![](../.gitbook/assets/image%20%286%29.png)

Lets look at the code and see how it is implemented.

Originally we started out with this.

![](../.gitbook/assets/image%20%281%29.png)

with a neural network to have an input layer in the shape of our data, and output layer in the shape of the number of categories we're trying to define, and a hidden layer in the middle. 

The Flatten takes our square 28 \* 28 images and turns them into a one dimensional array. = \[28 \* 28, 1\]

To add convolutions to this, you use code like this. 

![](../.gitbook/assets/image%20%2847%29.png)

You'll see that the last three lines are the same, the Flatten, the Dense hidden layer with 128 neurons, and the Dense output layer with 10 neurons. What's different is what has been added on top of this. Let's take a look at this, line by line. 

Here we're specifying the first convolution. We're asking keras to generate 64 _**filters**_ for us. 

These filters are 3 by 3, their activation is relu, which means the negative values will be thrown way, and finally the input shape is as before, the 28 by 28. That extra 1 just means that we are tallying using a single byte for color depth. As we saw before our image is our gray scale, so we just use one byte. 

Now, of course, you might wonder what the 64 filters are. They start with a set of known good filters in a similar way to the pattern fitting that you saw earlier, and the ones that work from that set are learned over time.

### Next line

This next line of code will then create a pooling layer. It's max-pooling because we're going to take the maximum value. We're saying it's a two-by-two pool, so for every four pixels, the biggest one will survive as shown earlier. We then add another convolutional layer, and another max-pooling layer so that the network can learn another set of convolutions on top of the existing one, and then again, pool to reduce the size. So, by the time the image gets to the flatten to go into the dense layers, it's already much smaller. It's being quartered, and then quartered again. So, its content has been greatly simplified, the goal being that the convolutions will filter it to the features that determine the output. A really useful method on the model is the model.summary method.

![](../.gitbook/assets/image%20%2813%29.png)

This allows you to inspect the layers of the model, and see the journey of the image through the convolutions, and here is the output. It's a nice table showing us the layers, and some details about them including the output shape. It's important to keep an eye on the output shape column. When you first look at this, it can be a little bit confusing and feel like a bug. After all, isn't the data 28 by 28, so why is the output, 26 by 26. 

![](../.gitbook/assets/image%20%288%29.png)

The key to this is remembering that the filter is a three by three filter. Consider what happens when you start scanning through an image starting on the top left. So, for example with this image of the dog on the right, you can see zoomed into the pixels at its top left corner. You can't calculate the filter for the pixel in the top left, because it doesn't have any neighbors above it or to its left. In a similar fashion, the next pixel to the right won't work either because it doesn't have any neighbors above it. So, logically, the first pixel that you can do calculations on is this one, because this one of course has all eight neighbors that a three by three filter needs. This when you think about it, means that you can't use a one pixel margin all around the image, so the output of the convolution will be two pixels smaller on x, and two pixels smaller on y.

{% hint style="info" %}
**Note**:

If your filter is five-by-five for similar reasons, your output will be four smaller on x, and four smaller on y. So, that's y with a three by three filter, our output from the 28 by 28 image, is now 26 by 26, we've removed that one pixel on x and y, and each of the borders.
{% endhint %}

{% embed url="https://youtu.be/vq2nnJ4g6N0" %}

So, next is the first of the max-pooling layers. Now, remember we specified it to be two-by-two, thus turning four pixels into one, and having our x and y. So, now our output gets reduced from 26 by 26, to 13 by 13. The convolutions will then operate on that, and of course, we lose the one pixel margin as before, so we're down to 11 by 11, add another two-by-two max-pooling to have this rounding down, and went down, down to five-by-five images. So, now our dense neural network is the same as before, but it's being fed with five-by-five images instead of 28 by 28 ones. But remember, it's not just one compress five-by-five image instead of the original 28 by 28, there are a number of convolutions per image that we specified, in this case 64. So, there are 64 new images of five-by-five that had been fed in. Flatten that out and you have 25 pixels times 64, which is 1600. So, you can see that the new flattened layer has 1,600 elements in it, as opposed to the 784 that you had previously. This number is impacted by the parameters that you set when defining the convolutional 2D layers. Later when you experiment, you'll see what the impact of setting what other values for the number of convolutions will be, and in particular, you can see what happens when you're feeding less than 784 over all pixels in. Training should be faster, but is there a sweet spot where it's more accurate? Well, let's switch to the workbook, and we can try it out for ourselves.

For more details on convolutions and how they works, check out the videos below:

{% embed url="https://www.youtube.com/playlist?list=PLkDaE6sCZn6Gl29AoE31iwdVwSG-KnDzF" %}



{% embed url="http://playground.tensorflow.org/\#activation=tanh&batchSize=10&dataset=circle&regDataset=reg-plane&learningRate=0.03&regularizationRate=0&noise=0&networkShape=4,2,1,2&seed=0.32924&showTestData=false&discretize=false&percTrainData=50&x=true&y=true&xTimesY=false&xSquared=false&ySquared=false&cosX=false&sinX=false&cosY=false&sinY=false&collectStats=false&problem=classification&initZero=false&hideText=false" %}





