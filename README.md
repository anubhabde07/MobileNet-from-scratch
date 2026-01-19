### Architecture Overview

This implementation follows the MobileNet design principle of using
**depthwise separable convolutions** to reduce computational cost.

Each block consists of:
1. **Depthwise Convolution** – applies a single convolution per input channel
2. **Batch Normalization**
3. **ReLU / ReLU6 activation**
4. **Pointwise (1×1) Convolution** – combines channel-wise features

Compared to standard CNNs, this design significantly reduces:
- Number of parameters
- Floating point operations (FLOPs)
- Memory usage

This makes the model suitable for **mobile and edge devices**.
