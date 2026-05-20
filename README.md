# BERT-base-uncased for Bislish Cyberbullying Detection

This repository contains the Jupyter notebook used for the thesis:

**Cyberbullying Detection in Code-Switched Bislish (Bisaya-English) Texts Using Fine-Tuned BERT-base-uncased**

The notebook includes the implementation for fine-tuning BERT-base-uncased for binary cyberbullying detection in Bislish social media text.

## Study Overview

This study fine-tuned BERT-base-uncased to classify Bislish social media text as either:

- Cyberbullying
- Non-cyberbullying

Bislish refers to Bisaya-English code-switched text commonly found in informal online communication.

The final dataset used in the study contained 2,377 unique social media posts and comments after duplicate removal. The dataset consisted of 1,273 cyberbullying instances and 1,104 non-cyberbullying instances.

## Fine-Tuning Strategies

The notebook includes two fine-tuning strategies:

1. **Full Fine-Tuning**  
   All parameters of BERT-base-uncased were updated during training.

2. **Layer Freezing**  
   The embedding layer and the first eight BERT encoder layers were frozen, while the final four encoder layers and classification head were trained.

Both strategies were trained and evaluated using the same dataset split, preprocessing pipeline, tokenizer, model architecture, training configuration, and evaluation metrics.

## Model

The model used in this study was:

- BERT-base-uncased
- 12 transformer encoder layers
- 768 hidden dimensions
- 12 attention heads
- Binary classification head

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- Weighted F1-score
- Misclassification analysis
- Wilcoxon signed-rank test

## Results Summary

Full Fine-Tuning achieved a higher average weighted F1-score than Layer Freezing. However, the Wilcoxon signed-rank test showed that the difference between the two strategies was not statistically significant at the 0.05 level.

Misclassification analysis showed that the models struggled with context-dependent Bislish expressions, including self-directed strong words, harmless expressive language, vague references, implied mockery, and indirect targeting.

## Repository Contents

```text
BERT_Bislish_Cyberbullying_Detection.ipynb
README.md
