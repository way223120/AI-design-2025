# NanoGPT - Text Generation based on *Blessing* ("祝福")

This project utilizes a customized implementation of **NanoGPT** for text generation, trained on the Chinese literary work *Blessing* ("祝福") by Lu Xun. The goal of this model is to generate text that imitates the style and tone of the original work.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Training Details](#training-details)
- [Results](#results)

## Introduction

This repository contains a project where **NanoGPT** (a simplified version of GPT) is used to train a model on a dataset based on the novel *Blessing* ("祝福") by Lu Xun. The trained model can generate text that resembles the style of the original work. The model is implemented using **PyTorch** and is structured to handle a custom dataset.

## Features
- **Text Generation**: Generates text in the style of the novel *Blessing* based on a user-provided starting text.
- **Custom Dataset**: Trained specifically on the Chinese text from *Blessing* ("祝福").
- **NanoGPT Model**: A transformer-based architecture inspired by GPT, designed for efficient training on smaller datasets.
  
## Getting Started

### Prerequisites
Before running the project, make sure you have the following installed:
- Python 3.x
- PyTorch
- NumPy

Additionally, you'll need the **Blessing** dataset saved as `祝福.txt`. You can download or prepare the dataset yourself.

### Usage

Place your 祝福.txt dataset in the root directory of the repository (same directory as Entrance Exam.ipynb).
Run the model training.
After training is completed, you can generate text using the model.
The script will output a text generation that continues from the provided start_text.

## Model Architecture
The architecture for this model is based on the NanoGPT framework, which is a simplified transformer-based architecture.

Key components of the model include:
Embedding Layers: Two embeddings are used — one for the token (characters) and another for the position within the sequence.
Transformer Blocks: The model utilizes a stack of transformer encoder layers with multi-head attention to handle dependencies across input tokens.
Output Layer: A final linear layer projects the model's hidden states to the vocabulary size to predict the next token.

Key Hyperparameters:
n_layer: The number of transformer layers (default: 8).
n_head: The number of attention heads in each transformer block (default: 8).
n_embd: The size of the token embeddings (default: 256).
block_size: The maximum length of the input sequences (set to 128 in this case).
The model uses multi-head self-attention to allow for efficient handling of long-range dependencies, making it capable of generating coherent, contextually relevant text.

## Training Details
Dataset: The training data is based on the text from Blessing ("祝福") by Lu Xun.
Model Configuration: NanoGPT with 8 layers, 8 attention heads, and 256 embedding size.

Training Parameters:
Optimizer: Adam with a learning rate of 1e-3.
Loss Function: Cross-Entropy Loss.
Epochs: The model is trained for 10 epochs to ensure the model captures the intricacies of the writing style.

Training involves tokenizing the input text and passing it through the transformer model, where the model learns to predict the next character in the sequence.

## Results
After training, the model can generate text in the style of *Blessing* ("祝福").
The generated text demonstrates the model's ability to produce coherent passages that align with the themes and tone of the original work.
