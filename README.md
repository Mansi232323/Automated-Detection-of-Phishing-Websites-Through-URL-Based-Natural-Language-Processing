# 🛡️ Automated Detection of Phishing Websites Through URL-Based Natural Language Processing

An intelligent machine-learning and deep-learning based system for the **automated detection of phishing and legitimate websites using URL-based analysis**.

The project investigates whether the structure, patterns, lexical characteristics, and sequential representation of a URL can be used to identify potentially malicious websites without relying exclusively on webpage content.

The system evaluates multiple Machine Learning, Deep Learning, and Transformer-based models across **large-scale URL datasets**, including experiments involving approximately **1.56 lakh, 5 lakh, and 15 lakh URLs**.

# 📖 Project Overview

Phishing is one of the most common cybersecurity threats in which attackers create malicious websites or URLs that imitate legitimate websites in order to deceive users.

A phishing URL may attempt to:

* Steal login credentials
* Capture personal information
* Collect financial information
* Redirect users to malicious websites
* Distribute malware
* Perform social engineering attacks
* Impersonate trusted organizations

Traditional phishing detection systems may depend on:

* Blacklists
* Website content
* Domain reputation
* Manual inspection
* Browser-based security mechanisms

However, URL-based analysis provides an important alternative because a URL itself contains many potentially useful characteristics.

For example:

```text
https://example.com/login
```

can be analyzed according to:

* Length
* Domain
* Number of special characters
* Number of subdomains
* Presence of suspicious keywords
* Number of digits
* Character patterns
* URL structure
* Token sequence
* Path characteristics
* Query parameters

This project therefore investigates **URL-based Natural Language Processing and Machine Learning techniques** for automated phishing website detection.

---

# 🎯 Problem Statement

The primary problem addressed by this project is:

> **To develop an automated system capable of distinguishing phishing URLs from legitimate URLs using URL-based features, machine-learning algorithms, deep-learning architectures, and Transformer-based Natural Language Processing techniques.**

The project aims to determine whether a URL can be treated as a sequence of meaningful characters/tokens and whether these patterns can be learned automatically by classification models.

---

# 💡 Motivation

The motivation behind this project is the increasing number of malicious and phishing URLs generated across the internet.

A phishing detection system should ideally be:

* Automated
* Fast
* Scalable
* Accurate
* Capable of processing large volumes of URLs
* Less dependent on manually maintained blacklists
* Capable of identifying previously unseen URL patterns

Therefore, this project experiments with datasets of different scales:

```text
1.56 Lakh URLs
       ↓
5 Lakh URLs
       ↓
15 Lakh URLs
```

This allows the project to move from a detailed model comparison toward **large-scale URL classification and scalability analysis**.

---

# 🎯 Objectives

The major objectives of this project are:

### 1. Automated Phishing Detection

Develop a system that automatically classifies URLs as phishing or legitimate.

### 2. URL-Based Analysis

Use characteristics contained within URLs instead of relying only on webpage content.

### 3. Machine Learning Comparison

Compare different traditional Machine Learning algorithms.

### 4. Deep Learning Comparison

Investigate whether sequence-based Deep Learning models can learn useful URL representations.

### 5. Transformer-Based NLP

Evaluate Transformer architectures for URL classification.

### 6. Large-Scale Evaluation

Experiment with datasets ranging from approximately **1.56 lakh to 15 lakh URLs**.

### 7. Performance Evaluation

Compare models using:

* Accuracy
* Precision
* Recall
* F1-score
* Training Loss
* Testing Loss
* Training Time where available

### 8. Identify the Best Model

Determine the strongest-performing architecture for the evaluated dataset and experimental setup.

---

# ⭐ Key Features

* URL-based phishing detection
* Binary classification
* Large-scale URL datasets
* Common Crawl URL data
* PhishTank URL data
* Feature-based Machine Learning
* Sequence-based Deep Learning
* Transformer-based NLP
* Multiple model comparison
* Accuracy analysis
* Precision analysis
* Recall analysis
* F1-score analysis
* Training/testing loss analysis
* Large-scale experimentation

---

# 📊 Dataset Overview

The project uses URL datasets at multiple scales.

The major dataset sizes considered in the project are:

| Dataset       | Approximate Size | Purpose                                                   |
| ------------- | ---------------: | --------------------------------------------------------- |
| **1.56 Lakh** |    ~156,000 URLs | Detailed ML, DL and Transformer evaluation                |
| **5 Lakh**    |    ~500,000 URLs | Large-scale URL experimentation                           |
| **15 Lakh**   |  ~1,500,000 URLs | Very large-scale Common Crawl + PhishTank experimentation |

---

# 🌐 Data Sources

The project uses URL information from sources including:

### Common Crawl

Common Crawl provides a very large collection of web crawl data that can be used to obtain legitimate web URLs.

### PhishTank

PhishTank provides phishing-related URL information that can be used for malicious/phishing URL examples.

The combination can be represented as:

```text
                 URL DATA
                    │
        ┌───────────┴───────────┐
        │                       │
        ▼                       ▼
   Common Crawl             PhishTank
        │                       │
        ▼                       ▼
 Legitimate URLs           Phishing URLs
        │                       │
        └───────────┬───────────┘
                    ▼
             Combined Dataset
                    │
                    ▼
              Classification
```

---

# 📦 Dataset Scale

One of the important aspects of this project is the use of progressively larger datasets.

## 1.56 Lakh

Approximately:

**156,000 URLs**

This experiment contains the most detailed model comparison, including traditional Machine Learning, Deep Learning, and Transformer approaches.

---

## 5 Lakh

Approximately:

**500,000 URLs**

This represents a significant increase in dataset size and allows large-scale Machine Learning experimentation.

---

## 15 Lakh

Approximately:

**1,500,000 URLs**

This is the largest dataset scale used in the project and includes URL data associated with **Common Crawl and PhishTank**.

---

# 🧹 Data Preprocessing

Before training the models, URLs need to be prepared appropriately.

The preprocessing pipeline includes the following general stages:

```text
Raw URL Data
     │
     ▼
Data Loading
     │
     ▼
Data Cleaning
     │
     ▼
Data Validation
     │
     ▼
URL Preprocessing
     │
     ▼
Feature Extraction / Tokenization
     │
     ▼
Train-Test Split
     │
     ▼
Model Training
     │
     ▼
Evaluation
```

The objective of preprocessing is to transform raw URL strings into representations that can be processed by Machine Learning and Deep Learning algorithms.

---

# 🔍 URL Feature Engineering

Traditional Machine Learning models use structured URL characteristics.

Potential URL characteristics considered in the project include:

* URL length
* Domain length
* Path length
* Number of dots
* Number of slashes
* Number of hyphens
* Number of digits
* Number of special characters
* Number of subdomains
* Presence of suspicious patterns
* URL structure
* Character-level properties

These characteristics allow traditional models to work with numerical representations of URLs.

---

# 🧠 URL Representation

The project explores two major ways of representing URLs.

## 1. Feature-Based Representation

Used primarily for traditional Machine Learning.

```text
URL
 ↓
Feature Extraction
 ↓
Numerical Feature Vector
 ↓
Machine Learning Model
 ↓
Prediction
```

---

## 2. Sequence-Based Representation

Used for Deep Learning and NLP models.

```text
URL
 ↓
Tokenization
 ↓
URL Sequence
 ↓
Embedding / Representation
 ↓
Deep Learning Model
 ↓
Prediction
```

This makes it possible to investigate whether Deep Learning models can automatically learn useful patterns from URL sequences.

---

# 🤖 Machine Learning Models

The project evaluates multiple Machine Learning algorithms.

The evaluated models include:

1. Linear Regression
2. Logistic Regression
3. Naive Bayes
4. Decision Tree
5. Random Forest
6. LightGBM
7. XGBoost
8. AdaBoost
9. Hybrid Ensemble
10. KNN
11. Linear SVC
12. Voting Classifier

These models provide a broad comparison between:

* Linear models
* Probabilistic models
* Tree-based models
* Boosting algorithms
* Ensemble methods

---

# 🧠 Deep Learning Models

The project also evaluates several Deep Learning architectures.

These include:

* ANN
* RNN
* LSTM
* GRU
* 1D CNN
* BiLSTM + Attention
* Hybrid Deep Learning Model

These architectures are particularly useful for sequential URL representations.

---

# 🔥 Why Deep Learning for URLs?

URLs can be treated as sequences of characters or tokens.

For example:

```text
https://example.com/login?id=123
```

can be represented as a sequence:

```text
h → t → t → p → s → : → / → / → ...
```

or as meaningful tokens.

This allows sequence models to learn patterns associated with phishing URLs.

---

# 🤗 Transformer Models

The project also explores Transformer-based Natural Language Processing approaches.

The evaluated Transformer models shown in the results include:

* BERT
* RoBERTa
* DistilBERT
* mBERT
* ALBERT
* TinyBERT

These models investigate whether contextual representations learned by Transformer architectures can be applied to URL classification.

---

# ⚙️ Experimental Setup

The overall experimental setup can be represented as:

```text
                 RAW URL DATA
                      │
                      ▼
              DATA PREPROCESSING
                      │
                      ▼
              FEATURE ENGINEERING
                      │
             ┌────────┴────────┐
             │                 │
             ▼                 ▼
       Feature-Based      Tokenized URL
             │                 │
             ▼                 ▼
      Machine Learning    Deep Learning
             │                 │
             │                 ▼
             │             Transformers
             │                 │
             └────────┬────────┘
                      ▼
                Classification
                      │
                      ▼
                  Evaluation
                      │
       ┌──────────────┼──────────────┐
       ▼              ▼              ▼
   Accuracy       Precision        Recall
                      │
                      ▼
                  F1-Score
```

---

# 📊 RESULTS — 1.56 LAKH DATASET

The **1.56 lakh dataset (~156,000 URLs)** was used for a comprehensive comparison of traditional Machine Learning, Artificial Neural Networks, recurrent architectures, CNNs, attention-based models, and Transformers.

---

## 📋 Complete Model Performance — 1.56 Lakh

| Model                  | Training Accuracy | Testing Accuracy | Training Loss | Testing Loss |  Precision |     Recall |   F1-Score |
| ---------------------- | ----------------: | ---------------: | ------------: | -----------: | ---------: | ---------: | ---------: |
| Logistic Regression    |            77.29% |           77.30% |        0.5147 |       0.5145 |     77.32% |     96.64% |     85.91% |
| Random Forest          |            88.07% |           85.63% |        0.2759 |       0.4516 |     86.45% |     94.80% |     90.43% |
| Linear SVC             |            77.21% |           77.27% |             — |            — |     76.90% |     97.57% |     86.01% |
| KNN                    |            87.57% |           83.05% |        0.3015 |       0.4079 |     85.85% |     91.39% |     88.53% |
| Gaussian Naive Bayes   |            75.71% |           76.56% |        0.5148 |       0.5140 |     77.04% |     95.81% |     85.41% |
| Decision Tree          |            86.97% |           85.02% |        0.3168 |       0.3299 |     86.36% |     93.92% |     89.98% |
| AdaBoost               |            77.66% |           77.72% |        0.5113 |       0.5108 |     77.65% |     96.72% |     86.14% |
| LightGBM               |            84.36% |           84.26% |        0.3649 |       0.3679 |     84.31% |     95.86% |     89.72% |
| XGBoost                |            85.01% |           84.84% |        0.3498 |       0.3553 |     84.91% |     95.85% |     90.05% |
| Voting Classifier      |            84.47% |           84.36% |        0.3637 |       0.3664 |     83.41% |     97.55% |     89.93% |
| ANN                    |            83.78% |           83.76% |        0.3778 |       0.3799 |     83.29% |     93.88% |     88.24% |
| RNN                    |            75.42% |           75.49% |        0.4851 |       0.4873 |     73.03% |     98.59% |     83.85% |
| LSTM                   |            97.48% |           96.52% |        0.0655 |       0.1041 |     95.84% |     99.02% |     97.41% |
| **1D CNN**             |        **97.71%** |       **96.76%** |    **0.0636** |       0.1170 | **96.02%** |     98.90% |     97.44% |
| GRU                    |            97.53% |           96.55% |        0.0660 |       0.1164 |     95.76% | **99.09%** |     97.39% |
| **BiLSTM + Attention** |            97.60% |           96.70% |        0.0644 |       0.1058 |     95.92% |     99.02% | **97.45%** |
| Transformer            |            93.78% |           93.45% |        0.1616 |       0.1685 |     92.34% |     98.23% |     95.19% |
| Hybrid DL Model        |            97.64% |           96.66% |        0.0636 |   **0.1035** |     95.88% |     99.02% |     97.42% |

---

# 🏆 Best Results — 1.56 Lakh

## 🥇 Highest Testing Accuracy

### 1D CNN

**Testing Accuracy: 96.76%**

| Metric            |      Score |
| ----------------- | ---------: |
| Training Accuracy | **97.71%** |
| Testing Accuracy  | **96.76%** |
| Training Loss     | **0.0636** |
| Testing Loss      |     0.1170 |
| Precision         | **96.02%** |
| Recall            |     98.90% |
| F1-Score          | **97.44%** |

---

# 🥇 Highest F1-Score

### BiLSTM + Attention

**F1-Score: 97.45%**

| Metric            |      Score |
| ----------------- | ---------: |
| Training Accuracy |     97.60% |
| Testing Accuracy  |     96.70% |
| Training Loss     |     0.0644 |
| Testing Loss      |     0.1058 |
| Precision         |     95.92% |
| Recall            |     99.02% |
| **F1-Score**      | **97.45%** |

---

# 🥇 Highest Recall

### GRU

**Recall: 99.09%**

| Metric            |      Score |
| ----------------- | ---------: |
| Training Accuracy |     97.53% |
| Testing Accuracy  |     96.55% |
| Training Loss     |     0.0660 |
| Testing Loss      |     0.1164 |
| Precision         |     95.76% |
| **Recall**        | **99.09%** |
| F1-Score          |     97.39% |

---

# 🧠 Deep Learning Top Performers

| Model                  | Testing Accuracy |  Precision |     Recall |   F1-Score |
| ---------------------- | ---------------: | ---------: | ---------: | ---------: |
| **1D CNN**             |       **96.76%** | **96.02%** |     98.90% |     97.44% |
| **BiLSTM + Attention** |           96.70% |     95.92% |     99.02% | **97.45%** |
| Hybrid DL              |           96.66% |     95.88% |     99.02% |     97.42% |
| GRU                    |           96.55% |     95.76% | **99.09%** |     97.39% |
| LSTM                   |           96.52% |     95.84% |     99.02% |     97.41% |
| Transformer            |           93.45% |     92.34% |     98.23% |     95.19% |

---

# 📊 RESULTS — 5 LAKH DATASET

The project also includes experimentation using approximately **5 lakh URLs (~500,000 URLs)**.

This dataset represents an intermediate scale between the 1.56-lakh and 15-lakh experiments.

The 5-lakh experiment is part of the project's large-scale URL analysis and provides a larger data environment for evaluating phishing detection techniques.

### Important

The material provided here confirms the **5-lakh dataset as part of the project**, but does not provide a complete 5-lakh model-results table.

Therefore, exact 5-lakh:

* Accuracy
* Precision
* Recall
* F1-score
* Training Loss
* Testing Loss

should be added from the corresponding experiment output rather than estimated.

---

# 📊 RESULTS — 15 LAKH DATASET

The project also uses approximately:

# **15 LAKH URLs**

or approximately:

# **1.5 Million URLs**

The provided result specifically describes:

> **15 Lakh URLs from CommonCrawl and PhishTank**

This experiment is used for large-scale Machine Learning evaluation.

---

# 🤖 Machine Learning Results — 15 Lakh URLs

| Model               |   Accuracy |  Precision |     Recall |   F1-Score |
| ------------------- | ---------: | ---------: | ---------: | ---------: |
| Linear Regression   |     65.59% |     65.94% |     60.11% |     62.89% |
| Logistic Regression |     65.73% |     65.90% |     60.77% |     63.23% |
| Naive Bayes         |     56.72% |     65.89% |     22.30% |     33.32% |
| Decision Tree       |     91.54% |     91.46% |     91.07% |     91.26% |
| **Random Forest**   | **95.55%** | **95.56%** | **95.26%** | **95.41%** |
| LightGBM            |     88.13% |     87.37% |     88.28% |     87.83% |
| XGBoost             |     92.29% |     91.91% |     92.22% |     92.07% |
| AdaBoost            |     72.78% |     73.38% |     68.86% |     71.05% |
| Hybrid Ensemble     |     78.24% |     87.00% |     64.82% |     74.29% |

---

# 🏆 Best Model — 15 Lakh Dataset

## Random Forest

Random Forest achieved the best reported overall performance in this Machine Learning experiment.

### ⭐ Accuracy: **95.55%**

### ⭐ Precision: **95.56%**

### ⭐ Recall: **95.26%**

### ⭐ F1-Score: **95.41%**

---

# 📊 15 Lakh Model Ranking

| Rank | Model               |   Accuracy |   F1-Score |
| ---: | ------------------- | ---------: | ---------: |
|   🥇 | **Random Forest**   | **95.55%** | **95.41%** |
|   🥈 | XGBoost             |     92.29% |     92.07% |
|   🥉 | Decision Tree       |     91.54% |     91.26% |
|    4 | LightGBM            |     88.13% |     87.83% |
|    5 | Hybrid Ensemble     |     78.24% |     74.29% |
|    6 | AdaBoost            |     72.78% |     71.05% |
|    7 | Logistic Regression |     65.73% |     63.23% |
|    8 | Linear Regression   |     65.59% |     62.89% |
|    9 | Naive Bayes         |     56.72% |     33.32% |

---

# 🤖 Transformer Results

The project also includes a dedicated Transformer-model comparison.

The reported models are:

* BERT
* RoBERTa
* DistilBERT
* mBERT
* ALBERT
* TinyBERT

---

# 📊 Consolidated Transformer Performance

| Rank | Model       |   Accuracy | Precision | Recall |   F1-Score | Training Time |
| ---: | ----------- | ---------: | --------: | -----: | ---------: | ------------: |
|    1 | **RoBERTa** | **96.20%** |    96.68% | 95.49% | **96.08%** |    537.27 sec |
|    2 | DistilBERT  |     95.50% |    95.48% | 95.29% |     95.38% |    327.44 sec |
|    3 | mBERT       |     93.30% |    92.53% | 93.85% |     93.18% |    812.79 sec |
|    4 | TinyBERT    |     92.70% |    92.78% | 92.21% |     92.49% | **62.85 sec** |
|    5 | BERT        |     92.80% |    92.44% | 92.83% |     92.63% |    483.50 sec |
|    6 | ALBERT      |     92.20% |    90.04% | 94.47% |     92.20% |    392.59 sec |

---

# 🥇 Best Transformer — RoBERTa

Among the reported Transformer models, **RoBERTa** achieved the highest accuracy.

### **Accuracy = 96.20%**

It also achieved:

* Precision = **96.68%**
* Recall = **95.49%**
* F1-score = **96.08%**

Therefore, RoBERTa was the strongest-performing Transformer in the reported comparison.

---

# ⚡ Fastest Transformer — TinyBERT

Although TinyBERT did not achieve the highest accuracy, it had the lowest reported training time.

### **Training Time = 62.85 seconds**

This highlights an important trade-off:

```text
Higher Performance
       ↕
Computational Cost
```

A model may provide very high accuracy while requiring more training resources, whereas a smaller model may train considerably faster.

---

# 🔬 Transformer Comparison

| Model       |   Accuracy |   F1-Score | Training Time |
| ----------- | ---------: | ---------: | ------------: |
| **RoBERTa** | **96.20%** | **96.08%** |      537.27 s |
| DistilBERT  |     95.50% |     95.38% |      327.44 s |
| mBERT       |     93.30% |     93.18% |      812.79 s |
| TinyBERT    |     92.70% |     92.49% |   **62.85 s** |
| BERT        |     92.80% |     92.63% |      483.50 s |
| ALBERT      |     92.20% |     92.20% |      392.59 s |

---

# 🏆 Overall Best Reported Models

Based strictly on the results provided:

| Category                            | Best Model             |   Best Result |
| ----------------------------------- | ---------------------- | ------------: |
| **1.56 Lakh — Testing Accuracy**    | **1D CNN**             |    **96.76%** |
| **1.56 Lakh — F1-Score**            | **BiLSTM + Attention** |    **97.45%** |
| **1.56 Lakh — Recall**              | **GRU**                |    **99.09%** |
| **1.56 Lakh — Lowest Testing Loss** | **Hybrid DL Model**    |    **0.1035** |
| **15 Lakh — ML Accuracy**           | **Random Forest**      |    **95.55%** |
| **15 Lakh — ML F1-Score**           | **Random Forest**      |    **95.41%** |
| **Transformer — Accuracy**          | **RoBERTa**            |    **96.20%** |
| **Transformer — F1-Score**          | **RoBERTa**            |    **96.08%** |
| **Transformer — Fastest Training**  | **TinyBERT**           | **62.85 sec** |

---

# 📈 Overall Dataset Comparison

| Dataset       | Approx. URLs | Main Experiment             | Best Reported Model      |        Best Reported Metric |
| ------------- | -----------: | --------------------------- | ------------------------ | --------------------------: |
| **1.56 Lakh** |        ~156K | ML + DL + Transformer       | 1D CNN                   | **96.76% Testing Accuracy** |
| **5 Lakh**    |        ~500K | Large-scale URL experiment  | Result not provided here |                           — |
| **15 Lakh**   |        ~1.5M | Common Crawl + PhishTank ML | Random Forest            |         **95.55% Accuracy** |

---

# 🔍 Detailed Performance Analysis

## Traditional Machine Learning

Traditional Machine Learning models showed varying performance.

The linear and probabilistic models generally produced lower accuracy in the reported large-scale experiment.

For example:

* Logistic Regression: **65.73%**
* Linear Regression: **65.59%**
* Naive Bayes: **56.72%**

Tree-based models performed considerably better:

* Decision Tree: **91.54%**
* XGBoost: **92.29%**
* Random Forest: **95.55%**

This indicates that the relationships between URL characteristics and phishing labels can be complex and non-linear.

---

# 🌲 Random Forest Analysis

Random Forest was the strongest reported traditional Machine Learning model.

Its performance:

```text
Accuracy  → 95.55%
Precision → 95.56%
Recall    → 95.26%
F1-Score  → 95.41%
```

The close relationship between precision and recall indicates a balanced classification performance in the reported experiment.

---

# 🧠 Deep Learning Analysis

The Deep Learning models showed particularly strong results in the 1.56-lakh experiment.

The highest-performing group was:

```text
1D CNN
BiLSTM + Attention
Hybrid DL
GRU
LSTM
```

All of these models achieved approximately **96.5%+ testing accuracy**.

Their F1-scores were also approximately **97%**, demonstrating strong overall classification performance.

---

# 🔄 Sequence Learning Analysis

RNN-based architectures such as:

* RNN
* LSTM
* GRU
* BiLSTM + Attention

were used to investigate sequential URL patterns.

The basic RNN achieved lower performance than the more advanced recurrent architectures.

The transition can be observed as:

```text
RNN
 ↓
LSTM / GRU
 ↓
BiLSTM + Attention
```

The reported results show a substantial improvement when moving from the basic RNN to more advanced sequence architectures.

---

# 🧩 Attention-Based Learning

BiLSTM + Attention achieved the highest reported F1-score:

### **97.45%**

Attention mechanisms allow the architecture to place greater importance on informative portions of the sequence.

For URL analysis, this is useful because specific parts of a URL may contain stronger phishing indicators than others.

---

# 🧬 CNN-Based URL Analysis

The 1D CNN achieved:

### **96.76% Testing Accuracy**

CNN-based architectures can identify local patterns in sequences.

For URL classification, these patterns may correspond to combinations of characters or tokens that frequently occur in suspicious URLs.

---

# 🤗 Transformer Analysis

The Transformer experiment demonstrates that pretrained NLP architectures can also be applied to URL sequences.

Among the evaluated models:

### RoBERTa performed best.

```text
Accuracy  = 96.20%
Precision = 96.68%
Recall    = 95.49%
F1-Score  = 96.08%
```

This demonstrates the potential of contextual Transformer representations for URL-based phishing detection.

---

# 📊 Complete Experimental Comparison

The overall research direction can be summarized as:

```text
                 PHISHING URL DETECTION
                         │
                         ▼
              ┌────────────────────┐
              │ Multiple Data Sizes │
              └─────────┬──────────┘
                        │
          ┌─────────────┼─────────────┐
          ▼             ▼             ▼
      1.56 Lakh       5 Lakh       15 Lakh
          │             │             │
          ▼             ▼             ▼
       ML + DL       Large Scale   Common Crawl
      + Transformer      Study      + PhishTank
          │                           │
          ▼                           ▼
      Model Study                ML Comparison
          │                           │
          └─────────────┬─────────────┘
                        ▼
                 PERFORMANCE
                   ANALYSIS
```

---

# 🚀 Scalability Analysis

One of the major strengths of this project is that it does not restrict experimentation to a single small dataset.

The project progresses through:

### **1.56 Lakh → 5 Lakh → 15 Lakh URLs**

This represents a substantial increase in the amount of data.

| Scale     | Approximate Data |
| --------- | ---------------: |
| 1.56 Lakh |          156,000 |
| 5 Lakh    |          500,000 |
| 15 Lakh   |        1,500,000 |

The largest dataset therefore contains approximately **1.5 million URLs**.

This scale provides an opportunity to investigate how URL-based phishing detection approaches behave as the amount of available data increases.

---

# 🧪 Evaluation Metrics

The project uses several evaluation metrics.

## Accuracy

Measures the overall proportion of correctly classified URLs.

```text
Accuracy =
Correct Predictions / Total Predictions
```

---

## Precision

Measures how many URLs predicted as phishing are actually phishing.

High precision means fewer false-positive predictions.

---

## Recall

Measures how many actual phishing URLs are successfully detected.

Recall is especially important in phishing detection because failing to identify a phishing URL can have serious consequences.

---

## F1-Score

F1-score provides a balance between precision and recall.

```text
F1 = 2 × (Precision × Recall)
     -------------------------
       Precision + Recall
```

---

## Training Loss

Training loss represents the model's error during training.

---

## Testing Loss

Testing loss provides information about model performance on unseen data.

---

# 🗂️ Project Structure

A suitable repository structure for the project is:

```text
Automated-Detection-of-Phishing-Websites-Through-URL-Based-Natural-Language-Processing/
│
├── README.md
│
├── MY_kaggle.ipynb
│
├── 15_lakh_dataset/
│   └── ...
│
├── 15_lakh_dataset_commoncrawl/
│   └── ...
│
├── 5_lakh_DL_Common_Crawl/
│   └── ...
│
├── 5_lakh_ML_Common_Crawl/
│   └── ...
│
└── results/
    └── ...
```

---

# 🛠️ Technologies Used

The project is based on Python and Machine Learning / Deep Learning technologies.

### Programming

* Python

### Data Processing

* Pandas
* NumPy

### Machine Learning

* Scikit-learn
* Random Forest
* Logistic Regression
* Decision Tree
* KNN
* Naive Bayes
* SVC
* AdaBoost
* Voting Classifier

### Gradient Boosting

* XGBoost
* LightGBM

### Deep Learning

* Neural Networks
* RNN
* LSTM
* GRU
* CNN
* BiLSTM
* Attention

### NLP / Transformers

* BERT
* RoBERTa
* DistilBERT
* mBERT
* ALBERT
* TinyBERT

---

# 🔬 Research Contribution

The project provides a broad experimental study of URL-based phishing detection by combining:

### 1. Multiple Dataset Scales

```text
156K → 500K → 1.5M URLs
```

### 2. Multiple ML Algorithms

Traditional feature-based approaches are compared.

### 3. Multiple Deep Learning Architectures

Sequence-based models are evaluated.

### 4. Transformer-Based NLP

Modern contextual language models are investigated for URL classification.

### 5. Comparative Evaluation

Models are compared using multiple performance metrics rather than accuracy alone.

---

# 🏆 Key Findings

Based on the reported results:

### Finding 1

The **1D CNN** achieved the highest testing accuracy in the 1.56-lakh model comparison:

> **96.76%**

### Finding 2

**BiLSTM + Attention** achieved the highest reported F1-score:

> **97.45%**

### Finding 3

**GRU** achieved the highest reported recall:

> **99.09%**

### Finding 4

**Random Forest** was the strongest reported traditional ML model in the 15-lakh experiment:

> **95.55% Accuracy**

### Finding 5

**RoBERTa** achieved the strongest reported Transformer accuracy:

> **96.20%**

### Finding 6

**TinyBERT** had the lowest reported Transformer training time:

> **62.85 seconds**

---

# ⚠️ Important Experimental Note

The different dataset experiments should not be interpreted as a perfectly controlled benchmark because the reported experiments differ in:

* Dataset size
* Feature representation
* URL representation
* Model family
* Experimental configuration

Therefore, the results are best interpreted as **separate experimental evaluations** rather than a single universal leaderboard.

In particular:

```text
1.56 Lakh results
        ≠
5 Lakh results
        ≠
15 Lakh results
```

unless all experimental conditions are kept identical.

---

# 🏁 Conclusion

This project presents a comprehensive approach toward **Automated Detection of Phishing Websites Through URL-Based Natural Language Processing**.

Rather than relying on a single classification algorithm, the project investigates a broad range of approaches, including:

* Traditional Machine Learning
* Ensemble Learning
* Deep Learning
* Recurrent Neural Networks
* CNNs
* Attention mechanisms
* Transformer architectures

The project also investigates URL datasets at multiple scales:

### **1.56 Lakh URLs**

providing a detailed comparison of ML, DL, and Transformer architectures.

### **5 Lakh URLs**

providing an intermediate large-scale URL experimentation environment.

### **15 Lakh URLs**

providing a very large-scale dataset involving **Common Crawl and PhishTank** URL data.

The strongest reported results include:

| Experimental Area      | Best Model             |     Result |
| ---------------------- | ---------------------- | ---------: |
| 1.56 Lakh — Accuracy   | **1D CNN**             | **96.76%** |
| 1.56 Lakh — F1         | **BiLSTM + Attention** | **97.45%** |
| 1.56 Lakh — Recall     | **GRU**                | **99.09%** |
| 15 Lakh — ML Accuracy  | **Random Forest**      | **95.55%** |
| Transformer — Accuracy | **RoBERTa**            | **96.20%** |

Overall, the experiments demonstrate the potential of **URL-based Machine Learning, Deep Learning, and NLP techniques for automated phishing detection**, while the use of datasets ranging from approximately **156,000 to 1.5 million URLs** provides a strong large-scale experimental foundation for the project.
