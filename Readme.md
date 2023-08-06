# Fake News Classifier

This repository contains a machine learning script for predicting whether a news article is potentially unreliable (Fake) or not (Real). The script uses natural language processing techniques and logistic regression for the task.

## Getting Started

These instructions will help you understand the content of the repository.

## Repository Structure

The repository contains a Jupyter notebook script (ipynb) which has been broken down into multiple sections to aid readability and understanding.

## Prerequisites

To run this script, you need to have the following libraries:

1. numpy
2. pandas
3. re
4. nltk
5. scikit-learn

You can install these libraries using pip:

```bash
pip install numpy pandas nltk scikit-learn regex
```

You will also need to download the `stopwords` corpus from nltk using the following command in your Python environment:

```python
import nltk
nltk.download('stopwords')
```

## Dataset

The script uses a dataset from a `train.csv` file. This dataset contains various details about news articles, including a unique ID, title, author, text, and a label marking the article as potentially unreliable (1) or reliable (0).

## Script Overview

The script begins with loading the dataset, replacing null values with empty strings, and merging the author's name and news title into a new column called 'content'. This content is then stemmed and converted into numerical data using TF-IDF Vectorizer.

The data is then split into training and test datasets. 80% of the data is used for training the Logistic Regression model and 20% is used for testing its performance.

The accuracy of the model on both training and testing data is printed as output. 

Finally, a predictive system is built which takes a news article as input and predicts whether the article is potentially unreliable or not.

## Running the script

The script can be run in any Python environment that supports the libraries. Jupyter notebooks or Google colab is recommended for easy visualization and debugging.

## Results

The accuracy of the model on the training and testing data is printed as output. The predictive system uses the trained model to classify a new news article as real or fake.

