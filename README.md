# Text Clustering Using BERT Embeddings

This repository provides a Python script for clustering text data using BERT embeddings. The code includes steps for generating BERT embeddings from text data, saving these embeddings, and preparing them for further analysis.

## Features

- **Dependency Installation**: Instructions for installing required libraries.
- **Data Loading and Preprocessing**: Loads and preprocesses text data.
- **BERT Embedding Generation**: Uses BERT to generate embeddings for the text data.
- **Embedding Saving**: Saves the generated embeddings for future use.

## Dataset

The dataset used for this project can be downloaded from [Hugging Face - AG News](https://huggingface.co/datasets/fancyzhx/ag_news/viewer).

## Generated Embeddings

You can download the generated embeddings from the following links:

- [Training Data Embeddings](https://drive.google.com/file/d/1zCVZ5I56L6YNbOZHI05C2JPUK3fd4fVq/view?usp=sharing)
- [Test Data Embeddings](https://drive.google.com/file/d/11f7dwhEIrgs0xNKQxe3V2DVA3_lrLMv8/view?usp=drive_link)

## Prerequisites

Ensure you have the following dependencies installed:

- `torch`
- `transformers`
- `numpy`
- `pandas`
- `scikit-learn`
- `matplotlib`
- `nltk`

Install them via `pip`:

```bash
!pip uninstall torch torch_xla -y
!pip install torch transformers
