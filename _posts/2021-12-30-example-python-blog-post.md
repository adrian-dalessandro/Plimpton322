---
layout: post
title: "Python Post Demo: How To Make a Custom Tensorflow Layer"
tagline: "A paragraph borrowed from a tensorflow tutorial to demonstrate how code can be shared"
author: Adrian D'Alessandro
excerpt_separator: <!--more-->
tags: blog tensorflow python
---
The best way to implement your own layer is extending the tf.keras.Layer class and implementing:
1. \__init__ , where you can do all input-independent initialization
2. build, where you know the shapes of the input tensors and can do the rest of the initialization
3. call, where you do the forward computation
Note that you don't have to wait until build is called to create your variables, you can also create them in __init__. However, the advantage of creating them in build is that it enables late variable creation based on the shape of the inputs the layer will operate on. On the other hand, creating variables in __init__ would mean that shapes required to create the variables will need to be explicitly specified.

```python
# python code with syntax highlighting.
import tensorflow as tf

class MyDenseLayer(tf.keras.layers.Layer):
  def __init__(self, num_outputs):
    super(MyDenseLayer, self).__init__()
    self.num_outputs = num_outputs

  def build(self, input_shape):
    self.kernel = self.add_weight("kernel",
                                  shape=[int(input_shape[-1]),
                                         self.num_outputs])

  def call(self, input):
    return tf.matmul(input, self.kernel)

layer = MyDenseLayer(10)
```
