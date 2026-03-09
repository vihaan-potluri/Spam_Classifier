# Spam Email Classifier (NLP + Logistic Regression)

This project builds a machine learning model that detects spam emails using **natural language processing (NLP)** techniques and **Logistic Regression**.

The model converts email text into numerical features using the **Bag-of-Words representation**, then learns patterns that distinguish spam messages from legitimate emails.

---

## Project Overview

Spam detection is a classic text classification problem in machine learning. The goal is to automatically determine whether an email message is spam or legitimate (ham) based on its content.

This project demonstrates a complete NLP pipeline:

1. Data preprocessing
2. Text feature extraction
3. Train/test splitting
4. Model training
5. Model evaluation
6. Model interpretation

---

## Dataset

The dataset contains email messages with the following information:

- **Subject line**
- **Email body**
- **Spam label** (1 = spam, 0 = ham)

The subject and body are combined to form the full email text used by the model.

---

## Methodology

### 1. Text Preprocessing
Missing text values are replaced with empty strings, and the subject and body fields are combined into a single text feature.

### 2. Feature Extraction
The **Bag-of-Words** approach is implemented using `CountVectorizer`.

This converts email messages into numerical vectors representing word frequencies.

### 3. Model Training
A **Logistic Regression classifier** is trained on the vectorized text features to learn patterns that distinguish spam from legitimate emails.

### 4. Model Evaluation
The model is evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score

These metrics measure how effectively the classifier identifies spam emails.

---

## Results

The model achieved approximately:

- **Accuracy:** ~99%
- **Precision:** High
- **Recall:** High

This performance indicates that the model successfully identifies strong vocabulary patterns associated with spam emails.

---

## Model Interpretation

Because Logistic Regression is interpretable, we can examine the learned coefficients to identify which words most strongly influence spam classification.

Examples of words associated with spam include:

- replica
- watches
- payment
- bank
- http

These words frequently appear in promotional or suspicious email content.

---

## Technologies Used

- Python
- pandas
- scikit-learn
- matplotlib
- Jupyter Notebook

---

## Future Improvements

Possible extensions to this project include:

- Using **TF-IDF features**
- Adding **URL-based features**
- Detecting **phishing patterns**
- Building a **phishing risk scoring system**

These improvements will be explored in a future project focused on phishing detection.

---

This project was created as part of a machine learning portfolio demonstrating practical applications of NLP and classification models.
