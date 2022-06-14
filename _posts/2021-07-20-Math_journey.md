---
title: My journey into mathematics
tags: [Mathematics, Statistical learning]
style: fill
color: info # Available colors (choose one): primary / secondary / success / danger / warning / info / light / dark
description: What I have learned.   
katex: true
---
<head>

  ...

  <!--KaTeX-->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.12.0/dist/katex.min.css" integrity="sha384-AfEj0r4/OFrOo5t7NnNe46zW/tFgW6x/bCJG8FqQCEo3+Aro6EYUG4+cU+KJWu/X" crossorigin="anonymous">
  <script defer src="https://cdn.jsdelivr.net/npm/katex@0.12.0/dist/katex.min.js" integrity="sha384-g7c+Jr9ZivxKLnZTDUhnkOnsh30B4H0rpLUpJ4jAIKs4fnJI+sEnkvrMWph2EDg4" crossorigin="anonymous"></script>
  <script defer src="https://cdn.jsdelivr.net/npm/katex@0.12.0/dist/contrib/auto-render.min.js" integrity="sha384-mll67QQFJfxn0IYznZYonOWZ644AWYC+Pt2cHqMaRhXVrursRwvLnLaebdGIlYNa" crossorigin="anonymous"></script>
  <script>
      document.addEventListener("DOMContentLoaded", function() {
          renderMathInElement(document.body, {
              // ...options...
          });
      });
  </script>

</head>


<!-- KaTeX requires the use of the HTML5 doctype. Without it, KaTeX may not render properly -->
<html>
  <head>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/katex@0.15.3/dist/katex.min.css" integrity="sha384-KiWOvVjnN8qwAZbuQyWDIbfCLFhLXNETzBQjA/92pIowpC0d2O3nppDGQVgwd2nB" crossorigin="anonymous">

    <!-- The loading of KaTeX is deferred to speed up page rendering -->
    <script defer src="https://cdn.jsdelivr.net/npm/katex@0.15.3/dist/katex.min.js" integrity="sha384-0fdwu/T/EQMsQlrHCCHoH10pkPLlKA1jL5dFyUOvB3lfeT2540/2g6YgSi2BL14p" crossorigin="anonymous"></script>

    <!-- To automatically render math in text elements, include the auto-render extension: -->
    <script defer src="https://cdn.jsdelivr.net/npm/katex@0.15.3/dist/contrib/auto-render.min.js" integrity="sha384-+XBljXPPiv+OzfbB3cVmLHf4hdUFHlWNZN5spNQ7rmHTXpd7WvJum6fIACpNNfIR" crossorigin="anonymous"
        onload="renderMathInElement(document.body);"></script>
  </head>
</html>

{% katexmm %}

I understand mathematics as the most general description of a process. The generality of mathematics is such that there can be only one description of said process. If I'm correct, statistical learning cannot predict new math equations. In math, there is no training data. In my young career as a data scientist I have only used math as a general framework to understand processes. And natural language to communicate with computers. 

Statistical learning is a branch of mathematics. Statistical learning is to transform data into simpler mathematical concepts or models. Like transforming two paired data sets into a line. Or like grouping the data. 

Statistical learning is divided into supervised, unsupervised learning, and semi-supervised learning. Supervised learning infers a model from the behavior of a target, call it Y. Unsupervised learning infers a relationship between data with no target. Semi supervised learning combines labeled and unlabeled data. 

# Introduction to statistical learning. Chapter 3.
## Linear Regression
This chapter contains 7 sections. 
3.1 Simple Linear Regression: 
	A simple linear regression is a statistical learning process. Is to fit a straight line through a data frame. The data frame contains paired sets of data points. Normally, call the sets X, Y, Z...
	In the linear regression setting assume that the relationship between these sets of data is linear. 
	A simple linear regression takes the form of 
	$Y = \beta_0 + \beta_1X$
	
3.1.1 Estimating the Coefficients.
	The purpose of statistical learning is to infer the functional form of the relationship between a target and some predictors. We do not know the population coefficients. Using a sample of data, we estimate them.
	
$\hat\beta_1 = \cfrac {\sum_{i=1}^n (x_i - \bar x)(y_i - \bar y)} {\sum_{i=1}^n (x_i - \bar x)^2}$

$\hat\beta_0 = \bar y - \hat\beta_1 \bar x$

3.1.2 Assessing the accuracy of the coefficient estimates. 
We rely on a property of normal populations. We assume our population is normal. We assume our sample is random. There is a high probability the mean of our sample lies close to the mean of the population. A normal population contains most of its values within a few Standard Deviations from its mean. We are likely to sample those values. The mean of the population and the mean of the sample are likely to resemble. 

The Standard Error $SE$ is the deviation of all samples we can extract from a population. We can infer this number using 1 sample. 

$Var(\hat\mu) = \widehat{SE}(\hat\mu)^2 = \cfrac{\sigma^2}{n}$

Where $\sigma$ is the Standard deviation of the realizations of the sample $y_i$. And $\hat\mu$ is the sample mean. 

We assume we extracted a random sample. Meaning that the population mean should be within a few $\widehat{SE}$ away from our sample mean.

The Standard Error also allows us to infer the population coefficients. 

The standard errors of the coefficients represent the average change in the coefficients introduced by the error, $\epsilon$. That is why sigma squared ($\sigma^2$) is part of the standard error equation for both $\hat b_0$ and $\hat b_1$.

The standard error of the coefficients can be used to set a range of possible values in which $b_0$ and $b_1$ land. The error makes each sample to be different. Because the error is distributed normally we assume $\hat f$ is probably close to $f$. How close? 95% of the samples will have coefficients that are $\pm 2 SE$ away from the predicted coefficient.

3.1.3 Assessing the Accuracy of the model.
Relies on less assumptions. We want to describe the fit of the regression line to the target values. We can use a standarized metric the REsidual Standard Error $RSE$. We apply some transformations to the Residual Sum of Sqaures $RSS$. The $RSS$ is the distance of each prediction to its corresponding target. 

$RSS = {\sum_i^n (\hat y_i - y_i)^2}$

$RSE = \sqrt{\cfrac {1} {2 - n} RSS} = \sqrt{\cfrac {1} {2 - n} {\sum_i^n (\hat y_i - y_i)^2}}$

$R^2$ is the proportion between the $RSS$ and the Total Sum of Squares $TSS$. The $TSS$ is the squared difference between each arget value and the mean of the target values.

$TSS = \sum{_i^n (y_i - \bar y)^2}$

$R^2 = \cfrac {TSS - RSS} {TSS} = 1 - \cfrac {RSS} {TSS}$

The $TSS$ is always greater than the $RSS$. A line that fits data points perfectly, has an $RSS$ close to 0. Divide that by the $TSS$ and you get a small number. Substract the small number from 1 and you get $R^2$. It is the proportion between the distance of $yi$ to the regression line, and the distance of $yi$ to the average line. The regression line is a slope. The average line is vertical. If $R^2$ is 0, total distances are similar. The regression line is not reducing the distance more than the average line. 

## 3.2 Multiple Linear regression
considers more predictors. Multiple Linear Regression gives each predictor an impact on the slope of the geometrical form used to fit the data. In three dimensions the geometrical form is plane. In higher dimensions it's hard to imagine. 

Multiple Linear regression expands the simple model. 

$Y = \beta_0 + \beta_1 X_1 + \beta_2 X_2 + ... + \beta_p X_p + \epsilon$

$\beta_j$ represents the average effect on the slope of a unit increase in $X_j$

3.2.1 Estimating the coefficients

$\hat y = \hat\beta_0 + \hat\beta_1 x_1 + \hat\beta_2 x_2 + ... + \hat\beta_p x_p$

# Neural networks
A neural network (NN) is a node based system. It receives a numeric input. The NN feeds the input to a number of randomized regression machines. The machines produce and output and feed the output to a second layer of regression machines. The final outcome is squished and fed into the last node. A Neural network can do many tasks including statistical learning and signal transmission. Tensorflow and Keras lead the way. 

A Neural Network resembles a brain. In its least abstract layer, a brain communicates with electrical signals. They open electrical doors. As time progresses the system learns to distribute the electrical signals correctly. Wrong signals will happen as the system learns.

OpenAI is a deep learning model. It performs multiple operations on a set of predictors to output a token $\hat y_i$. The predictors are the context of $\hat y_i$ and are represented as variables. Tokens represent characters. Those characters form human readable combinations. $\hat y$ are the most probable tokens given the context. 

{% endkatexmm %}
