# NLP and Sequence Modeling Mini Project

## Project Objective

The objective of this project is to build an NLP pipeline for customer support sentiment classification.

The project demonstrates:
- text preprocessing
- TF-IDF vectorization
- Logistic Regression baseline model
- sequence modeling concepts using LSTM
- attention and transformer reflections

---

# Dataset Description

Dataset File:
customer_support_text_classification.csv

Target Column:
- sentiment_label

Target Classes:
- positive
- neutral
- negative

Input Text Column:
- customer_message

Additional Features:
- channel
- word_count
- urgent_flag

---

# Task 1 : Dataset Understanding

The dataset contains customer support messages categorized into sentiment classes.

Dataset Statistics:
- Total Records: 1500
- Total Columns: 6
- Average Text Length: 72.75 characters

Class Distribution:
- neutral: 524
- negative: 497
- positive: 479

The dataset is relatively balanced across all sentiment categories.

---

# Task 2 : Text Preprocessing

The following preprocessing steps were performed:

1. Lowercasing
2. Removing special characters
3. Tokenization
4. Stopword removal

Example:

Original Text:
"I need information about the payment process."

Processed Text:
"need information payment process"

---

# Task 3 : Text Vectorization

TF-IDF vectorization was used to convert text into numerical form.

Why vectorization is required:
Machine learning models cannot understand raw text directly.
Text must be converted into numerical vectors before model training.

TF-IDF helps:
- measure word importance
- reduce influence of common words
- improve classification performance

Feature Matrix Shape:
- (1500, 146)

---

# Task 4 : Baseline Model

Baseline Model:
- Logistic Regression
- TF-IDF Features

Evaluation Metrics:
- accuracy
- classification report
- confusion matrix

Final Accuracy:
- 100%

The model achieved perfect classification on the testing dataset.

---

# Confusion Matrix Analysis

The confusion matrix shows:
- all sentiment classes were predicted correctly
- no major misclassification occurred

This indicates:
- strong text separability
- effective preprocessing
- highly informative TF-IDF features

---

# Task 5 : Sequence Model

Sequence Model:
- LSTM (Long Short-Term Memory)

Architecture:
1. Input Sequence
2. Embedding Layer
3. LSTM Layer
4. Dropout Layer
5. Dense Output Layer

Loss Function:
- sparse categorical crossentropy

Evaluation Metric:
- accuracy

---

# Why Sequence Modeling Is Important

Traditional vectorization methods ignore word order.

Sequence models:
- preserve text sequence
- capture context
- understand relationships between words

Example:
- "not good"
- "good"

These sentences contain similar words but opposite meanings.

LSTMs can understand such contextual differences.

---

# Task 6 : Attention and Transformer Reflection

## Why RNNs struggle with long-term dependencies?

RNNs process words sequentially.
During long sequences:
- earlier information gets forgotten
- gradients vanish during training

Therefore RNNs struggle with long-term memory.

---

## How LSTMs help with memory?

LSTMs use:
- memory cells
- forget gates
- input gates
- output gates

These mechanisms help preserve important information over long sequences.

---

## What does attention solve?

Attention helps models focus on important words in the sequence.

Instead of treating all words equally,
the model learns which words are most relevant for prediction.

---

## Why transformers are important?

Transformers use self-attention mechanisms.

Benefits:
- parallel processing
- better context understanding
- faster training
- improved long-range dependency learning

Transformers power modern Generative AI systems such as:
- ChatGPT
- Gemini
- Claude
- BERT

---

# Technologies Used

- Python
- TensorFlow
- Keras
- Scikit-learn
- NLTK
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

# Conclusion

This project successfully demonstrated:
- NLP preprocessing
- text vectorization
- sentiment classification
- TF-IDF modeling
- Logistic Regression
- LSTM sequence architecture
- transformer concepts

The project highlights the importance of sequence modeling in modern NLP and Generative AI systems.