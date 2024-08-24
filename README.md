# News Headline Generation

## Project Overview
This project implements a Seq2Seq model with an Attention Mechanism for generating news headlines from article text. Additionally, it fine-tunes the T5 (Text-To-Text Transfer Transformer) large language model to improve headline generation performance, with a focus on optimizing the METEOR metric. The project aims to produce headlines that are both contextually accurate and concise, effectively summarizing the main content of news articles.

## Introduction
Generating news headlines is a challenging task that requires understanding and summarizing the content of an article in a few words. This project tackles the problem using a Seq2Seq Encoder-Decoder architecture with an Attention Mechanism, enabling the model to focus on relevant parts of the input text while generating headlines. Additionally, the project explores the fine-tuning of a pre-trained T5 model, which has been specifically adapted to text generation tasks, optimizing for the METEOR metric to ensure high-quality outputs.

## Dataset
The dataset used in this project consists of pairs of news articles and their corresponding headlines. The dataset includes diverse news categories such as politics, sports, technology, and entertainment, providing a comprehensive training set for the model. The dataset is preprocessed to remove noise and standardize the input text.

## Installation
To run this project, you need Python 3.x installed along with the following libraries:

- pandas
- numpy
- PyTorch
- Transformers (for T5 model)
- NLTK
- METEOR
- tqdm

You can install the required packages using pip:
```bash
pip install pandas numpy tensorflow keras transformers nltk rouge meteor-score
