---
layout: post
title:  "How Edge Detection Works"
categories: feature extraction, feature detection
---

How do computers find edges in an image?

<img src="/images/posts/edge-detection.png" height="auto" width="48%">
<img src="/images/post-covers/how-edge-detection-works.jpg" height="auto" width="48%">

Of course, to a human this is a trivial task. But to a computer, all that it "sees" is a collection of RGB values.

One popular technique is called the Sobel operator.

## Kernels & Convolutions

### Kernel
In image processing, a kernel is also called a "mask" or "filter".

This is kernel/mask/filter for horizontal edge detection:

This is a kernel for vertical edge detection:

### Convolution

+ Padding
+ Stride



<a title="By Michael Plotke (Own work) [CC BY-SA 3.0 (https://creativecommons.org/licenses/by-sa/3.0)], via Wikimedia Commons" href="https://commons.wikimedia.org/wiki/File%3A3D_Convolution_Animation.gif"><img width="256" alt="3D Convolution Animation" src="https://upload.wikimedia.org/wikipedia/commons/4/4f/3D_Convolution_Animation.gif"/></a>

[GIF Credit](http://amitkushwaha.co.in/images/cropped_max_pooling.gif)

### Still curious?

+ [How Blurs & Filters Work](https://www.youtube.com/watch?v=C_zFhWdM4ic)    
+ [Sobel Operator](https://www.youtube.com/watch?v=uihBwtPIBxM&t=31s)
+ [Kernels in Image Processing](https://en.wikipedia.org/wiki/Kernel_(image_processing))
+ [Detecting a Cell Using Image Segmentation](https://www.mathworks.com/help/images/detecting-a-cell-using-image-segmentation.html)
+ [Images as Functions](http://ai.stanford.edu/~syyeung/cvweb/tutorial1.html)
+ [Paper on Canny Edge Detection](http://cmp.felk.cvut.cz/~cernyad2/TextCaptchaPdf/A%20Computational%20Approach%20to%20Edge%20Detection.pdf)
