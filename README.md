# MLP with Attention mechanism for cyberattacks detection.

This repository hosts the code related to the paper, Paying Attention to cyber-attacks: A multi-layer perceptron with self-attention mechanism

The paper addresses the problem of detecting violent actions in videos, analyzing the state of the art of various deep learning models and developing a new one. Our aim is to develop a new neural network model capable of reaching or exceeding the state of the art.

## Abstract

Cyber-attacks cause huge monetary losses to the institutions that are victims of them. Therefore,
the protection system against cyber-attacks has become a highly requested resource by any type
of state or private institution. During the pandemic caused by COVID-19, the number of cyber-
attacks against both public and private health institutions has increased. Cybersecurity systems
have become a necessity. Various protection systems have been proposed using different machine
learning algorithms, but deep learning consistently provides the best results. In this work we
develop a deep learning model for the detection of different kinds of cyber-attacks, a study
is carried out on the relevance of the selection of features in this type of algorithm and the
importance of attention mechanisms is analyzed to improve the assessment of features within
the same model. We have carried out the experiments using two datasets that are benchmarks in
the field of cybersecurity and we have carried out a comparative study with both.

## Requirements

This project is implemented in Python using the [Tensorflow](https://www.tensorflow.org/) libraries to develop the model.

- OpenCV v4.4.0.46
- Ipython v7.16.1
- Scikit-Image v0.17.2
- Scikit-Learn v0.24.2
- Tensorflow v2.11.0
- Livelossplot v0.5.3
- Matplotlib v3.3.2
- Numpy v1.19.2

### Install the repository:

```
git clone https://github.com/FernandoJRS/mlp-attention-cyber-attacks
```

### Install the requirements:

```
pip install -r requirements.txt
```

## Model Architecture

The following graph shows the architecture of our model.

![Model Architecture](figures/MultiheadSelfAttentionMLP.png?raw=True "Model Architecture")

Multi-head Self Attention MLP Architecture. The input layer input_8 (InputLayer) is the input layer of the
model which receives the vector (𝑥1 ... 𝑥𝑛). The layers dense_38, dense_39, dense_40, and dense_41 compose the first
MLP module which together with the layer multi_head_attention_7 (MultiHeadAttention) perform the feature analysis.
The layers dense_42, dense_43, dense_44, and dense_45 compose the second MLP module that acts as a classifier.
Finally, the dense_46 layer is the output layer of the model, which implements the Softmax function and indicates to
which category the input vector belongs. The output layer is for binary classification in the case of binary subsets but
adapts to multi-class classification by modifying the output dimension by the number of attacks to be classified.

## Cyber-attack Detection System

The following graph shows the system pipeline for cyber-attacks detection.

![System Pipeline](figures/SystemModelPipelinev21.png?raw=True "System Pipeline")
