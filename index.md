---
layout: default
title: Hello World
---
# Welcome to Plimpton 322

## Code Demo

Below is a brief exerpt demonstrating code blocks:

```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
```

```python
# python code with syntax highlighting.
import tensorflow as tf

def fake_custom_loss(y_pred, y_true):
  return tf.keras.losses.mean_squared_error(y_pred, y_true)
```

## Latex Equation Demo

Below is a sample of how mathjax renders latex-stype equations:

$$\mathcal{L}_{MSE} = \sum_{i=1}^{m} \text{log}p(y^{(i)} | \mathbf{x}^{(i)}; \mathbf{\theta}) = \ m \text{log} (\sigma) - \frac{m}{2}\text{log}(2\pi) - \sum_{i=1}^m \frac{||\hat{y}^{(i)} - y^{(i)}||}{2\sigma^2}$$
