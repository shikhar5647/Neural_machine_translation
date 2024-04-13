# English-Hindi Neural Machine Translation

This repository contains the code for training and evaluating a neural machine translation (NMT) model for translating English text to Hindi using sequence-to-sequence models with attention mechanism.

## Introduction
Machine Translation is the task of automatically converting text or speech from one language into another. It has numerous applications in various fields such as communication, localization, and content translation. In this project, we focus on translating English sentences to Hindi, a widely spoken language in India.

## Preprocessing
The data preprocessing steps include:

Lowercasing: Converting all text to lowercase to ensure consistency.
Removing HTML Tags and URLs: Eliminating any HTML tags and hyperlinks present in the text.
Removing Special Characters and Punctuation: Removing non-alphanumeric characters and punctuation marks from the text.
Tokenization: Splitting the text into individual words or tokens.
Removing Stopwords: Eliminating common words (e.g., "the", "is", "and") that do not contribute much to the meaning of the text.
Stemming: Converting words to their root form (e.g., "running" to "run").

## Model Architecture
The model architecture consists of an encoder-decoder framework with LSTM (Long Short-Term Memory) layers. Here's a brief overview:

Encoder: Embedding layer followed by LSTM layer to encode input English sentences into a fixed-length vector representation.
Decoder: Embedding layer followed by LSTM layer to decode the encoded vector and generate the corresponding Hindi translations.
Loss Function: Sparse categorical cross-entropy, used to measure the difference between the predicted and actual outputs.
Optimizer: Adam optimizer, used to minimize the loss function during training.

## Training
The model is trained with the following configurations:
Batch Size: 32
Number of Epochs: 6
Early Stopping: Patience of 3 epochs, to prevent overfitting by stopping training if the validation loss does not improve for consecutive epochs.
Model Checkpoint: Saving the model weights with the best validation loss.

## Dataset

The dataset used for training and evaluation can be found on Kaggle: [English-Hindi Dataset](https://www.kaggle.com/datasets/preetviradiya/english-hindi-dataset)

## Requirements

- Python 3.x
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib (for visualization)
- Jupyter Notebook (optional, for running the provided notebooks)

## Usage

1. Clone this repository:

```bash
git clone https://github.com/shikhar5647/Neural_machine_translation.git
cd Neural_machine_translation

