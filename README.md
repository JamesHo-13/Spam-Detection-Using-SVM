# Spam Detection Using Support Vector Machines

## Overview

This project develops a machine learning model to classify text messages as **spam** or **not spam (ham)** using a Support Vector Machine (SVM) classifier.

Spam detection is a common application of natural language processing (NLP) and supervised learning. The goal of this project is to build a predictive model capable of identifying unwanted messages based on text characteristics and evaluate how effectively SVM methods can be applied to text classification problems.

---

## Author

**James Ho**

**Course:** Statistical Machine Learning / Data Science  
**Institution:** Colorado State University

---

# Motivation

With the increasing volume of digital communication, automated spam detection systems are essential for filtering unwanted messages and improving user experience.

Traditional rule-based filtering methods often struggle with changing spam patterns. Machine learning approaches can learn patterns from previously labeled messages and adapt to new examples.

This project explores the use of Support Vector Machines to classify messages by identifying important patterns in text data.

---

# Research Questions

This project investigates:

1. Can Support Vector Machines accurately classify spam messages?
2. Which text features are most useful for distinguishing spam from legitimate messages?
3. How does feature representation affect classification performance?
4. How well does the model generalize to unseen messages?

---

# Dataset

The dataset contains labeled text messages categorized as:

- **Spam** — unwanted or malicious messages
- **Ham** — legitimate messages

Each observation contains:

- Message text
- Classification label

The target variable is:

\[
Y =
\begin{cases}
1, & \text{Spam}\\
0, & \text{Ham}
\end{cases}
\]

---

# Data Processing

Before modeling, text data was processed through several preprocessing steps:

## Text Cleaning

Steps included:

- Converting text to lowercase
- Removing punctuation
- Removing unnecessary characters
- Removing stop words
- Cleaning inconsistent formatting

## Feature Extraction

Text messages were transformed into numerical features using:

### TF-IDF (Term Frequency–Inverse Document Frequency)

TF-IDF converts text into numerical vectors based on word importance.

The method considers:

- How frequently a word appears in a message
- How common or rare the word is across all messages

This creates a feature matrix suitable for machine learning algorithms.

---

# Model Development

## Support Vector Machine (SVM)

A Support Vector Machine classifier was used to separate spam and legitimate messages.

SVM works by finding an optimal decision boundary that maximizes the margin between classes.

Advantages of SVM for text classification:

- Effective in high-dimensional feature spaces
- Works well with sparse text data
- Provides strong classification performance
- Reduces overfitting through margin maximization

---

# Model Workflow

```
Raw Messages
      |
      v
Text Cleaning
      |
      v
TF-IDF Feature Extraction
      |
      v
Train/Test Split
      |
      v
Support Vector Machine
      |
      v
Spam Classification
      |
      v
Model Evaluation
```

---

# Model Evaluation

The model was evaluated using several classification metrics:

## Accuracy

Measures the percentage of correctly classified messages.

\[
Accuracy =
\frac{Correct Predictions}{Total Predictions}
\]

## Precision

Measures how many messages predicted as spam were actually spam.

## Recall

Measures how many actual spam messages were successfully detected.

## F1 Score

Balances precision and recall.

\[
F1 =
2 \times
\frac{Precision \times Recall}
{Precision + Recall}
\]

## Confusion Matrix

Used to analyze:

- True positives
- True negatives
- False positives
- False negatives

---

# Results

The SVM classifier successfully learned patterns in message text and demonstrated strong performance in separating spam from legitimate messages.

Important findings:

- TF-IDF effectively represented message content.
- SVM performed well with high-dimensional text features.
- The model was able to identify important language patterns associated with spam.
- Evaluation metrics showed reliable classification performance.

---

# Feature Analysis

The model analysis examined words and text patterns that contributed most strongly to classification.

Common spam indicators included:

- Promotional language
- Financial offers
- Urgent requests
- Prize-related terms
- Suspicious links or contact information

---

# Repository Structure

```
Spam-Detection-SVM/
│
├── Data/
│   └── spam_dataset.csv
│
├── Code/
│   └── Spam_Detection_SVM.R
│
├── Figures/
│   ├── confusion_matrix.png
│   ├── performance_metrics.png
│   └── feature_analysis.png
│
├── Report/
│   └── Spam_Detection_Report.pdf
│
└── README.md
```

---

# Technologies Used

## Programming Languages

- R

## Libraries

- e1071
- caret
- tm
- tidytext
- dplyr
- ggplot2

## Machine Learning Methods

- Support Vector Machines
- Text Classification
- TF-IDF Feature Extraction
- Supervised Learning
- Model Evaluation

---

# Future Improvements

Possible improvements include:

- Comparing SVM performance with:
  - Random Forest
  - Naive Bayes
  - Logistic Regression
  - Neural Networks
- Applying word embeddings such as Word2Vec or BERT
- Using larger and more diverse datasets
- Implementing real-time spam detection
- Performing hyperparameter optimization

---

# Conclusion

This project demonstrates the application of machine learning and natural language processing techniques to solve a real-world classification problem.

By combining TF-IDF text representation with Support Vector Machines, the model can effectively identify spam messages and demonstrates the usefulness of statistical learning methods for automated text classification.
