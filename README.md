# Text Clustering Using BERT Embeddings

## Overview

This repository provides a Python script for clustering text data using BERT embeddings. The code includes steps for generating BERT embeddings from text data, saving these embeddings, and preparing them for further analysis.

## Features

- **Dependency Installation**: Instructions for installing required libraries.
- **Data Loading and Preprocessing**: Loads and preprocesses text data.
- **BERT Embedding Generation**: Uses BERT to generate embeddings for the text data.
- **Embedding Saving**: Saves the generated embeddings for future use.

## Prerequisites

Ensure you have the following dependencies installed:

- `torch`
- `transformers`
- `numpy`
- `pandas`
- `scikit-learn`
- `matplotlib`
- `nltk`

You can install the required libraries using `pip`:

```bash
!pip uninstall torch torch_xla -y
!pip install torch transformers
