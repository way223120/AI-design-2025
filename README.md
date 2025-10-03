# NanoGPT - Text Generation based on *Blessing* ("祝福")

This project utilizes a customized implementation of **NanoGPT** for text generation, trained on the Chinese literary work *Blessing* ("祝福") by Lu Xun. The goal of this model is to generate text that imitates the style and tone of the original work.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Training Details](#training-details)
- [Results](#results)
- [License](#license)

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
- PyTorch (with CUDA support if you have a GPU)
- NumPy

Additionally, you'll need the **Blessing** dataset saved as `祝福.txt`. You can download or prepare the dataset yourself.

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/NanoGPT-Blessing.git
   cd NanoGPT-Blessing
