# NeuraNet

[**NeuraNet**](https://github.com/JamorMoussa/NeuraNet) is a deep learning library inspired by **Pytorch**, but built solely with **Math** and **Numpy**. It was created for academic purposes, aiming to provide a simple and readable implementation for those interested in understanding the inner workings of frameworks like **PyTorch** and **TensorFlow**.


The syntax of NeuraNet closely resembles that of PyTorch. Therefore, code written for building neural networks with NeuraNet will likely work with PyTorch with minimal modifications. However, PyTorch is a more complex framework that offers additional functionalities, such as accelerating model training using the power of GPUs through built-in CUDA support.

## Build a Neural Network

The NeuraNet library offers built-in functionalities, for building Neural Networks architectures. like `nn.Linear`, `nn.ReLU` ,etc. In fact, the NeuraNet offer a class `nn.Module` which is the base class for any Neural Networks models.

We have two ways to build a Neural Network. First, using `nn.Sequential` class. Second, by building class by extending the `nn.Module`.


### Using Sequential Model

```python
import neuranet as nnt
import neuranet.nn as nn

model = nn.Sequential(
    nn.Linear(2, 3),
    nn.ReLU(),
    nn.Linear(3, 1)
)
```

### By Extending `nn.Module`

```python

import neuranet as nnt
import neuranet.nn as nn


class NNet(nn.Module):

    def __init__(self) -> None:

        self.l1 = nn.Linear(2, 3)
        self.relu = nn.ReLU()
        self.l2 = nn.Linear(3, 1)

    def forward(self, input: nnt.Tensor):
        out = self.l1(input)
        out = self.relu(out)
        return self.l2(out)

```