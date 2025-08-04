# Project Overview

This repository demonstrates how to use a Naive Bayes classifier and fine-tune a BERT model to classify human-written vs. AI-generated text. The dataset, obtained from Kaggle, contains essays authored by humans and various AI models.

## File Structure

- **nlpProjectPt1.py**  
  Preprocesses the text and trains a Naive Bayes model using TF-IDF features.

- **nbInference.py**  
  Loads the Naive Bayes model saved in `nlp_project_pt1` and performs inference on new text.  
  _Usage:_ Download the saved model files and update the directory path in this script.

- **nlpProjectPt2.py**  
  Fine-tunes an uncased BERT classifier using Hugging Face’s `Trainer` API and saves the trained model.

- **bertInference.py**  
  Loads the fine-tuned BERT model from `nlp_project_pt2` and performs inference on new text.  
  _Usage:_ Download the `human-ai-model` folder and update the model directory path in this script.

- **final_split_dataset.csv**  
  Contains the preprocessed and split dataset used for training and evaluation in Part 2. This file also serves as an index for identifying false positives and false negatives.

## Metrics

### Naive Bayes

| Label        | Precision | Recall | F1-Score | Support |
|--------------|-----------|--------|----------|---------|
| Human        | 0.96      | 0.99   | 0.97     | 61159   |
| AI           | 0.97      | 0.93   | 0.95     | 36288   |
| **accuracy** |           |        | 0.96     | 97447   |
| **macro avg**| 0.97      | 0.96   | 0.96     | 97447   |
| **weighted avg** | 0.96  | 0.96   | 0.96     | 97447   |



### BERT

| Label        | Precision | Recall | F1-Score | Support |
|--------------|-----------|--------|----------|---------|
| Human        | 1.00      | 1.00   | 1.00     | 30442   |
| AI           | 1.00      | 1.00   | 1.00     | 18282   |
| **accuracy** |           |        | 1.00     | 48724   |
| **macro avg**| 1.00      | 1.00   | 1.00     | 48724   |
| **weighted avg** | 1.00  | 1.00   | 1.00     | 48724   |

[Project Plan](https://docs.google.com/document/d/1Lm1yaX8iE9ymeoc_OBfV6p1WH6OnHR5f-gI1CvL0r64/edit?usp=sharing)
[Project Report](https://docs.google.com/document/d/1sV1X0L6CpHxzN0HU2OvIhQHQErt6W9Abe7N3JTjeDvQ/edit?usp=sharing)
