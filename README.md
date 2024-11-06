# Clustering Text Using BERT Embeddings, Saving Embeddings, and Visualizing Clusters

## Overview

This repository demonstrates how to use BERT embeddings for clustering text data. The workflow includes:
- Preprocessing raw text data
- Generating embeddings using the BERT model
- Saving the embeddings for further analysis
- Visualizing the clusters using dimensionality reduction techniques like PCA

The project utilizes the `transformers` library to leverage BERT for generating text embeddings and `scikit-learn` for clustering the embeddings using KMeans.

## Prerequisites

To run the project, you need to install the following dependencies:

```bash
!pip uninstall torch torch_xla -y
!pip install torch transformers
```

In addition, you will need the following Python packages:
- `numpy`
- `pandas`
- `scikit-learn`
- `matplotlib`
- `nltk`

You can install them using `pip`:

```bash
pip install numpy pandas scikit-learn matplotlib nltk
```

## Project Structure

1. **Data Loading**: 
   - The dataset is loaded from two `.parquet` files: `train.parquet` and `test.parquet`.
   - The data should contain a `text` column with raw text data for preprocessing and embedding.

2. **Preprocessing**: 
   - The text data is cleaned by removing punctuation, converting to lowercase, and removing stopwords. 
   - You can choose between **stemming** or **lemmatization** for normalizing the text.

3. **Embedding Generation**:
   - BERT embeddings are generated using Hugging Face's `transformers` library with the `BertTokenizer` and `BertModel`.

4. **Clustering**:
   - KMeans clustering is applied to the generated BERT embeddings for grouping the text data into different clusters.

5. **Visualization**:
   - Dimensionality reduction using PCA is applied to the embeddings, and the clusters are visualized in a 2D space.

## Steps to Use

### 1. Data Loading

The dataset is loaded from `.parquet` files. Ensure your dataset files are named `train.parquet` and `test.parquet`. The files should contain a `text` column with raw text data.

### 2. Text Preprocessing

The text data is cleaned and normalized by removing punctuation, converting the text to lowercase, and removing stopwords. You can choose between **stemming** or **lemmatization** to normalize the words.

### 3. Generating BERT Embeddings

BERT embeddings are generated for the preprocessed text using the `BertTokenizer` and `BertModel` from Hugging Face's `transformers` library. These embeddings are then saved to `.npy` files for later use.

### 4. Saving Embeddings

After generating the BERT embeddings for both the training and test data, you can save them as `.npy` files. These saved embeddings can be used for downstream tasks like clustering or visualization.

### 5. Clustering

KMeans clustering is applied to the generated embeddings to group the data into clusters. You can adjust the number of clusters depending on the task and data.

### 6. Visualizing Clusters

To visualize the clusters, PCA is used to reduce the dimensionality of the embeddings. The clusters are then plotted in a 2D space using `matplotlib` to visualize how the data points are grouped.

## Dataset

The dataset used in this project is the [AG News dataset](https://huggingface.co/datasets/fancyzhx/ag_news) from Hugging Face. It contains news articles categorized into four classes: World, Sports, Business, and Science/Technology.

### Data Columns:
- **text**: The raw text of the news articles to be clustered.

## Results

- **Embeddings**: BERT-based embeddings are generated for each text entry, capturing semantic information about the content.
- **Clustering**: KMeans clustering groups the embeddings into predefined clusters.
- **Visualization**: PCA is used to reduce the dimensionality of the embeddings to 2D for visual inspection of the clusters.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
