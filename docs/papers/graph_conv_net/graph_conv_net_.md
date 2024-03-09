Graph Convolutional Networks by [**Moussa Jamor**](https://github.com/JamorMoussa)

# Semi-Supervised Classification with GCN


**Graph Convolutional Networks (GCN)** is graph-base neural network
architecture introduced by *Thomas N. Kipf* and *Max Welling* in their paper ti-
tled [<u>Semi-Supervised Classification with Graph Convolutional Networks</u>](https://arxiv.org/pdf/1609.02907v4.pdf) in 2017. As they mentioned in their paper, that this proposed architecture
is an effecient variant of Convolution Neural Network (CNN), and It’s the first-
order approximation of spectral graph convoltions.


## CGN Layers

In their paper [[2]](https://arxiv.org/pdf/1609.02907v4.pdf), *Thomas N. Kipf* and *Max Welling* introduce the concept of multi-layer graph convolutional networks (GCNs). They propose a layer-wise propagation rule defined by the equation $A$:

\\[
    H^{(l+1)} = \sigma\left(\widetilde{D}^{-\frac{1}{2}} \widetilde{A} \widetilde{D}^{-\frac{1}{2}} H^{(l)} W^{(l)}\right)
\\]


