# Multi-Domain Sentiment Analysis and Drug Prediction

A brief description of your project.

## Table of Contents

- [Project Title](#project-title)
- [Table of Contents](#table-of-contents)
- [Introduction](#introduction)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Preprocessing](#preprocessing)
- [Training](#training)
- [Evaluation](#evaluation)
- [Results](#results)
- [Model Deployment](#model-deployment)
- [Additional Resources](#additional-resources)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project is focused on performing Multi-Domain Sentiment Analysis using deep learning techniques. Sentiment analysis, also known as opinion mining, is the process of determining the emotional tone behind a piece of text. In this project, we analyze text data to determine whether the sentiment expressed in each piece of text is positive or negative.

# Getting Started

## Prerequisites

Before running the code in this project, make sure you have the following libraries and dependencies installed:

- Python 3.x
- TensorFlow
- Pandas
- Numpy

You can install them using pip:

```bash
  pip install tensorflow pandas numpy
```
# Dataset

The project uses a dataset for training and testing the sentiment analysis model. The dataset is stored in two separate files, one for training data and the other for testing data. The training data and testing data are loaded as Pandas DataFrames from CSV files.

## Data Preprocessing

The following data preprocessing steps are performed:

1. Columns that are not required for sentiment analysis are dropped.
2. The ratings in the dataset are converted to binary labels (1 for positive, 0 for negative).
3. The reviews are tokenized and padded to ensure consistent lengths for input data.

# Model

The deep learning model used for sentiment analysis is based on Long Short-Term Memory (LSTM) networks. The model architecture consists of:

- An Embedding layer
- A Dense hidden layer
- Dropout layers to prevent overfitting
- An LSTM layer
- Another Dropout layer
- A Dense output layer

The model is compiled using binary cross-entropy loss and the Adam optimizer.

## Training

The model is trained on the preprocessed data for a certain number of epochs. The training process provides insights into the loss and accuracy of the model.

## Model Export

The trained model is saved to a file using the pickle library. This saved model can be loaded and used for making sentiment predictions for new reviews.

# Usage

You can use the model to perform sentiment analysis on new reviews by calling the `predict_new_review` function. Provide the review text as input, and it will output whether the sentiment is positive or negative.

```python
predict_new_review(['Your new review text here'])
```
# Drug Prediction

The project includes a drug prediction model. Given a condition, review, rating, and useful count, it predicts the most suitable drug for the user. The prediction is based on a Wide & Deep Neural Network (W&DNN) model.

## Exporting Data

The data used for sentiment analysis can be exported to a CSV file for further analysis.

## Authors

- musaddique333

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

