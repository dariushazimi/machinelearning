# FAQ

## How to determine number of neurons needed?

trial and error, you can test with 64, 128, 512 and 1024. You'll see that higher number of neurons yields better learning but also leads to slower training of the model. The pay off on higher number of neurons slows down pretty quickly and 1024 performs marginally better than 512.

## What is convolution and pooling?

it usually involves having a filter and passing that filter over the image in order to change the underlying image. The process works a little bit like this. For every pixel, take its value, and take a look at the value of its neighbors. If our filter is three by three, then we can take a look at the immediate neighbor, so that you have a corresponding three by three grid. Then to get the new value for the pixel, we simply multiply each neighbor by the corresponding value in the filter. So, for example, in this case, our pixel has the value 192, and its upper left neighbor has the value zero. The upper left value and the filter is negative one, so we multiply zero by negative one. Then we would do the same for the upper neighbor. Its value is 64 and the corresponding filter value was zero, so we'd multiply those out. Repeat this for each neighbor and each corresponding filter value, and would then have the new pixel with the sum of each of the neighbor values multiplied by the corresponding filter value, and that's a convolution

![](../.gitbook/assets/image%20%288%29.png)

![](../.gitbook/assets/image%20%2819%29.png)

![](../.gitbook/assets/image%20%2811%29.png)

![](../.gitbook/assets/image%20%2817%29.png)

