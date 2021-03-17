---
layout: post
title: "Latex Equation Demo: Looking at Maximum A Posteriori Estimation"
tagline: "A paragraph borrowed from wikipediaa to demonstrate how latex-style equation editing works within this blog"
author: Borrowed Wikipedia Entry
excerpt_separator: <!--more-->
tags: blog theory stats
---
# Just An Example Post About Maximum Likelhood Estimation
ssume that we want to estimate an unobserved population parameter $$\theta$$ on the basis of observations $$x$$. Let $$f$$ be the sampling distribution of $$x$$, so that $$f(x|\theta)$$ is the probability of $$x$$ when the underlying population parameter is $$\theta$$. Then the function:
<!--more-->
$$\theta \mapsto f(x|\theta)$$ is known as the likelihood function and the estimate:

$$\hat{\theta}_{MLE}(x) =\underset{\theta}{\text{arg max}} f(x|\theta)$$

is the maximum likelihood estimate of $\theta$ .

Now assume that a prior distribution $g$ over $\theta$ exists. This allows us to treat {$\theta$  as a random variable as in Bayesian statistics. We can calculate the posterior distribution of $\theta$ using Bayes' theorem:

$$\theta \mapsto f(\theta|x) = \frac{f(x|\theta)g(\theta)}{\int_{\Theta} f(x|\vartheta)g(\vartheta)d\vartheta}$$

So on and so forth
