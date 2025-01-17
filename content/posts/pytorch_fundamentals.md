---
date: '2025-01-18T03:15:13+05:30'
title: PyTorch Fundamentals
subtitle: 'PyTorch 101: Laying the Groundwork for ML'
categories:
  - pytorch
math: true
tags:
  - fundamentals
editor_options: 
  markdown: 
    wrap: 72
---

## Importing PyTorch

Let's start by importing PyTorch and checking the version we're using.

```         
import torch
torch.__version__
```

```         
2.5.1+cu121
```

It looks like we've got PyTorch 2.5.1+.

------------------------------------------------------------------------

## Introduction to Tensors

Tensors are multi-dimensional arrays with a uniform type. In machine
learning, the term tensor informally refers to two different concepts
: 1. a way of organizing data and 2. a multilinear (tensor)
transformation. Data may be organized in a multidimensional array (M-way
array).

For example, you could represent an image as a tensor with shape
`[3, 224, 224]` which could mean `[colour_channels, height, width]`.
Thus, the tensor would have dimensions.

For a detailed explanation of tensors, you can refer to a video by Dan
Fleisch: [What's a
Tensor?](https://www.youtube.com/watch?v=f5liqUk0ZTw).

---
### Creating Tensors
There is a whole documentation page for the [`torch.Tensor`](https://pytorch.org/docs/stable/tensors.html) class.

Let's see a few of the data types which can be defined as :

`torch.float32` or `torch.float` for 32-bit floating point,

`torch.float64` or `torch.double` for 64-bit floating point,

`torch.complex64` or `torch.cfloat` for 64-bit complex point.

---

The first thing we're going to create is a **scalar**.

A scalar is a single number and in tensor-speak it's a zero dimension
tensor.

```         
# Scalar
scalar = torch.tensor(7)
scalar
```

```         
tensor(7)
```

That means although `scalar` is a single number, it's of type
`torch.Tensor`.

We can check the dimensions of a tensor using the `ndim` attribute.

```         
scalar.ndim
```

```         
0
```
