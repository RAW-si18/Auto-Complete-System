# N-Gram Language Model

This project implements an n-gram language model with k-smoothing to predict the next word in a sequence and evaluate the model using perplexity.

## Table of Contents

- [N-Gram Language Model](#n-gram-language-model)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Features](#features)
  - [Installation](#installation)
  - [Usage](#usage)
    - [Running the Notebook](#running-the-notebook)
  - [Examples](#examples)

## Introduction

The n-gram language model is a type of probabilistic language model for predicting the next item in a sequence, in this case, the next word in a sentence. The model uses k-smoothing to handle zero counts in n-gram probabilities and evaluates its performance using the perplexity metric.

## Features

- Predict the next word based on previous words using n-gram probabilities.
- Implement k-smoothing to handle unseen n-grams.
- Evaluate model performance with perplexity scores.
- Support for n-grams and (n+1)-grams.

## Installation

To use this project, follow these steps:

Clone the repository:
```sh
git clone https://github.com/RAW-si18/AUTO-COMPLETE-SYSTEM.git
```

## Usage

To use the n-gram model, open and run the Jupyter notebook `main.ipynb`. The notebook includes the following key functions:

- `estimate_probabilities`: Estimate probabilities of the next word.
- `suggest_next_word`: Suggest the most likely next word based on previous tokens.
- `compute_perplexity`: Calculate the perplexity of the model on a test set.

### Running the Notebook

1. Open the Jupyter notebook:
    ```sh
    jupyter notebook main.ipynb
    ```
2. Execute the cells in the notebook to train the model, predict the next word, and evaluate using perplexity.

## Examples

Here are a few example usages of the functions provided in the notebook:

- Predict the next word:
    ```python
    previous_tokens = ['i', 'like']
    suggestion, probability = suggest_next_word(previous_tokens, n_gram_counts, n_plus1_gram_counts, vocabulary, k=1.0)
    print(f"The suggested next word is '{suggestion}' with a probability of {probability:.4f}")
    ```

- Compute perplexity:
    ```python
    test_sentence = ['i', 'like', 'to', 'play', 'football']
    perplexity = compute_perplexity(test_sentence, n_gram_counts, n_plus1_gram_counts, vocabulary, k=1.0)
    print(f"The perplexity of the test sentence is {perplexity:.4f}")
    ```
