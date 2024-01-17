---
title: "A little knowledge about CNN"
date: 2024-01-14T23:21:10+07:00
draft: false
---
{{< katex >}}

# Convolutional Neural Network
Convolutional Neural Networks (CNNs) constitute a cornerstone in deep learning theory, specifically designed for processing grid-like data like images and video. The canonical architecture encompasses convolutional layers, where learnable filters convolve across input data, extracting hierarchical and spatial features. Subsequent pooling layers facilitate downsampling, enhancing translation invariance. These are often followed by fully connected layers and non-linear activation functions to model complex relationships. The complete suite of layers typically includes input layers, convolutional layers, pooling layers, fully connected layers, and output layers, collectively orchestrating the network's ability to learn intricate patterns and representations for diverse tasks such as image recognition and object detection.

The inception of Convolutional Neural Networks (CNNs) marked a significant milestone in neural network architecture, with the Neocognitron standing as a pioneering precursor to this revolutionary development. The Neocognitron paper introduced groundbreaking concepts such as feature extraction, pooling layers, and the integration of convolution within a neural network for recognition or classification purposes. Inspired by the visual nervous system of vertebrates, the Neocognitron structured its network with alternating layers of S-cells (simple cells or lower-order hypercomplex cells) and C-cells (complex cells or higher-order hypercomplex cells). This arrangement facilitated the repeated process of feature extraction by S-cells and positional shift tolerance by C-cells(see Figure 1). The network's overarching design, resembling the visual nervous system, enabled the gradual integration of local features into more global representations. Utilized for tasks like handwritten (Japanese) character recognition, the Neocognitron laid the foundation for subsequent Convolutional Neural Networks, influencing their application in diverse pattern recognition tasks.

{{< figure
    src="neocognitron.png"
    alt="Neocognitron Network"
    caption="Neocognitron Network created by Japanese"
    >}}



The idea of the convolution operation in a Convolutional layer might derive from the signal processing study. From two signals (or two functions), denoted by \\(f\\) and \\(g\\), we create the third function \\(f * g\\). This derived function intricately expresses the transformation of one function's shape under the influence of the other, emphasizing the interplay and modification of their respective mathematical structures.

{{< figure
    src="convOP.png"
    alt="convoOperation"
    caption="Signal pulses of function f and g and the result of the convolutional operation"
    >}}

# Two-dimensional convolutional layer

As mentioned above, convolution is a mathematical operation involving two functions
with a real-valued variable. In essence, the operation \\(*\\) is essentially the integration
of the product of two functions. However, in some computational-related fields, the
formula can be represented as discrete function, as others called discrete convolution:
$$s(t) = (x * w)(t) = \sum_{a= -\infty}^{\infty} x(a)w(t-a)$$

In this term, the variable x represents the input, while the variable w represents
the **kernel** or **filter**. The output s is often called the **output**.