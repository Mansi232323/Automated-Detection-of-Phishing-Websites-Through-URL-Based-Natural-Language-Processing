# 🛡️ Automated Detection of Phishing Websites Through URL-Based Natural Language Processing

## 📌 Project Overview

Phishing is a major cybersecurity threat in which attackers create deceptive websites and URLs to trick users into revealing sensitive information such as usernames, passwords, banking credentials, and other personal data.

This project focuses on developing an **automated phishing URL detection system** using **Natural Language Processing (NLP), Machine Learning (ML), Deep Learning (DL), and Transformer-based models**.

Instead of depending only on webpage content, the project analyzes the **URL itself** and learns patterns that can differentiate between:

* ✅ **Legitimate URLs**
* 🚨 **Phishing URLs**

The project was evaluated on **multiple large-scale URL datasets**, including:

* **1.56 Lakh URLs**
* **5 Lakh URLs**
* **15 Lakh URLs**

The **5 Lakh and 15 Lakh datasets were created using URLs from CommonCrawl and PhishTank**, allowing the system to be evaluated on a significantly larger and more diverse collection of URLs.

---

# 🎯 Problem Statement

The objective of this project is to develop an intelligent system that can automatically classify a URL as **legitimate or phishing** based on its structural and textual characteristics.

The system investigates whether URL patterns can be effectively learned using:

1. Traditional Machine Learning algorithms
2. Deep Learning architectures
3. NLP-based sequence models
4. Transformer architectures

The ultimate goal is to build a scalable phishing detection approach capable of processing **hundreds of thousands to millions of URLs**.

---

# 💡 Motivation

Phishing attacks continue to evolve, making static detection approaches less effective against newly generated malicious URLs.

A URL often contains useful information that can indicate suspicious behavior.

For example:

```text
https://example.com/login
```

and

```text
http://example-secure-login-example.xyz/verify/account
```

may have very different structural and lexical characteristics.

The project therefore investigates whether these characteristics can be learned automatically by computational models.

A major focus of the project is **scalability**.

Instead of evaluating the models on only a small dataset, experiments were conducted across progressively larger datasets:

```text
1.56 Lakh
     ↓
5 Lakh
     ↓
15 Lakh
```

This allows the project to investigate phishing detection at increasingly large scales.

---

# 🎯 Objectives

The main objectives of the project are:

### 1. Automated Phishing Detection

Develop an automated system capable of classifying URLs into phishing and legitimate categories.

### 2. URL-Based Classification

Use the URL itself as the primary source of information for classification.

### 3. Machine Learning Evaluation

Evaluate different traditional ML algorithms and compare their performance.

### 4. Deep Learning Evaluation

Investigate CNN, RNN, LSTM, GRU, BiLSTM, Attention, and hybrid architectures.

### 5. Transformer-Based NLP

Evaluate Transformer models for URL sequence classification.

### 6. Large-Scale Dataset Evaluation

Perform experiments on:

* **1.56 Lakh URLs**
* **5 Lakh URLs**
* **15 Lakh URLs**

### 7. Performance Comparison

Compare models using:

* Accuracy
* Precision
* Recall
* F1-score
* Training Loss
* Testing Loss
* Training Time, where available

### 8. Identify High-Performing Models

Determine the best-performing models for the reported experiments.

---

# 📊 Dataset Overview

The project uses datasets at three major scales.

| Dataset       | Approximate Number of URLs | Source                      | Purpose                                    |
| ------------- | -------------------------: | --------------------------- | ------------------------------------------ |
| **1.56 Lakh** |                   ~156,000 | Project dataset             | Detailed ML, DL and Transformer comparison |
| **5 Lakh**    |               **~500,000** | **CommonCrawl + PhishTank** | Large-scale experimentation                |
| **15 Lakh**   |             **~1,500,000** | **CommonCrawl + PhishTank** | Very large-scale ML experimentation        |

---

# 🌐 Data Sources

## 1. CommonCrawl

CommonCrawl provides large-scale web crawl data from which URLs can be collected.

In this project, CommonCrawl data contributes to the large-scale URL dataset.

---

## 2. PhishTank

PhishTank provides phishing URL data.

These URLs represent the **phishing/malicious class** used for phishing detection experiments.

---

# 📦 1.56 Lakh URL Dataset

The first major experimental dataset contains approximately:

# **1.56 Lakh URLs**

or approximately:

### **156,000 URLs**

This dataset was used for a detailed comparison between:

* Traditional Machine Learning
* Deep Learning
* Transformer models

The 1.56-lakh experiment provides the most extensive model-level comparison in the reported results.

---

# 📦 5 Lakh URL Dataset

The second major dataset contains approximately:

# **5 Lakh URLs**

or:

### **500,000 URLs**

### Source:

**CommonCrawl + PhishTank**

The 5-lakh dataset was specifically created using URL data from these two sources.

The dataset can therefore be represented as:

```text
                 5 LAKH URL DATASET
                         │
              ┌──────────┴──────────┐
              │                     │
              ▼                     ▼
         CommonCrawl             PhishTank
              │                     │
              ▼                     ▼
       Web URL Data          Phishing URL Data
              │                     │
              └──────────┬──────────┘
                         ▼
                  Combined Dataset
                         │
                         ▼
                   ~500,000 URLs
```

The purpose of using 5 lakh URLs is to provide a considerably larger dataset for evaluating the scalability of the phishing detection pipeline.

---

# 📦 15 Lakh URL Dataset

The largest dataset contains approximately:

# **15 Lakh URLs**

or:

### **1,500,000 URLs**

The dataset uses:

**CommonCrawl + PhishTank**

as its major URL sources.

This experiment extends the project from hundreds of thousands of URLs to approximately **1.5 million URLs**, providing a large-scale environment for evaluating Machine Learning models.

---

# 📈 Dataset Scale Comparison

| Dataset       |      Size | CommonCrawl | PhishTank |
| ------------- | --------: | :---------: | :-------: |
| **1.56 Lakh** |     ~156K |      —      |     —     |
| **5 Lakh**    | **~500K** |      ✅      |     ✅     |
| **15 Lakh**   | **~1.5M** |      ✅      |     ✅     |

The project therefore progresses from a detailed 156K experiment to large-scale 500K and 1.5M URL experiments.

---

# 🔄 Overall Project Workflow

```text
                  URL DATA COLLECTION
                          │
           ┌──────────────┴──────────────┐
           │                             │
           ▼                             ▼
      CommonCrawl                    PhishTank
           │                             │
           ▼                             ▼
     Web URL Data                 Phishing URLs
           │                             │
           └──────────────┬──────────────┘
                          ▼
                   DATA CLEANING
                          │
                          ▼
                  DATA PREPROCESSING
                          │
                          ▼
              FEATURE EXTRACTION /
                    TOKENIZATION
                          │
             ┌────────────┼────────────┐
             │            │            │
             ▼            ▼            ▼
        Machine        Deep         Transformer
        Learning      Learning          NLP
             │            │            │
             └────────────┼────────────┘
                          ▼
                    CLASSIFICATION
                          │
                          ▼
                     EVALUATION
                          │
           ┌──────────────┼──────────────┐
           ▼              ▼              ▼
       Accuracy       Precision        Recall
                          │
                          ▼
                       F1-Score
```

---

# 🧹 Data Preprocessing

Before model training, the collected URLs are processed to make them suitable for classification.

The preprocessing stage includes the general steps required for preparing URL data:

### 1. URL Collection

URLs are obtained from the relevant datasets.

### 2. Data Cleaning

Unusable or inappropriate URL records are removed.

### 3. Duplicate Handling

Duplicate URLs are handled to reduce unnecessary repetition in the dataset.

### 4. Label Assignment

URLs are assigned to their corresponding classes.

```text
Legitimate → 0
Phishing   → 1
```

### 5. URL Representation

URLs are converted into representations suitable for the selected model.

For Machine Learning:

```text
URL → Numerical Features
```

For Deep Learning/NLP:

```text
URL → Tokens → Sequence Representation
```

---

# 🔍 URL Feature Engineering

Traditional Machine Learning algorithms require numerical input.

Therefore, relevant characteristics can be extracted from URLs, such as:

* URL length
* Domain length
* Number of dots
* Number of slashes
* Number of digits
* Number of special characters
* Number of hyphens
* Number of subdomains
* Path characteristics
* Query characteristics
* Suspicious lexical patterns

The general process is:

```text
Raw URL
   ↓
Feature Extraction
   ↓
Numerical Feature Vector
   ↓
Machine Learning
   ↓
Prediction
```

---

# 🧠 URL as a Sequence

For Deep Learning and NLP models, the URL can be considered a sequence of characters or tokens.

For example:

```text
https://example.com/login
```

can be represented as a sequence of characters/tokens.

This makes URL data suitable for sequence-learning architectures such as:

* RNN
* LSTM
* GRU
* CNN
* BiLSTM
* Attention
* Transformer

---

# 🤖 Machine Learning Models

The project evaluates several Machine Learning algorithms, including:

* Linear Regression
* Logistic Regression
* Naive Bayes
* Decision Tree
* Random Forest
* LightGBM
* XGBoost
* AdaBoost
* KNN
* Linear SVC
* Voting Classifier
* Hybrid Ensemble

These models provide a comparison between:

* Linear approaches
* Probabilistic approaches
* Tree-based models
* Boosting algorithms
* Ensemble methods

---

# 🧠 Deep Learning Models

The Deep Learning experiments include:

* ANN
* RNN
* LSTM
* GRU
* 1D CNN
* BiLSTM + Attention
* Hybrid Deep Learning Model

These models allow the system to learn more complex patterns from URL sequences.

---

# 🤗 Transformer Models

The project also evaluates Transformer-based architectures:

* BERT
* RoBERTa
* DistilBERT
* mBERT
* ALBERT
* TinyBERT

These models are investigated for their ability to learn contextual representations from URL sequences.

---

# 📊 RESULTS — 1.56 LAKH DATASET

The 1.56-lakh experiment provides detailed results across Machine Learning, Deep Learning, and Transformer-based approaches.

## Complete Model Results

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

### 🥇 Highest Testing Accuracy

**1D CNN — 96.76%**

### 🥇 Highest F1-Score

**BiLSTM + Attention — 97.45%**

### 🥇 Highest Recall

**GRU — 99.09%**

### 🥇 Lowest Testing Loss

**Hybrid DL Model — 0.1035**

---

# 📊 Top Deep Learning Results

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

## Dataset Description

The project uses a dedicated dataset of approximately:

# **5 Lakh URLs (~500,000 URLs)**

collected from:

### **CommonCrawl + PhishTank**

The purpose of this dataset is to evaluate the phishing detection system at a larger scale than the 1.56-lakh experiment.

The 5-lakh dataset therefore represents an important intermediate stage in the project:

```text
1.56 Lakh
   ↓
5 Lakh
   ↓
15 Lakh
```

### Data Source

| Source               | Role              |
| -------------------- | ----------------- |
| **CommonCrawl**      | Web URL data      |
| **PhishTank**        | Phishing URL data |
| **Combined Dataset** | ~5 Lakh URLs      |

### 5-Lakh Dataset Pipeline

```text
CommonCrawl + PhishTank
          ↓
      URL Collection
          ↓
      Data Cleaning
          ↓
     URL Processing
          ↓
 Feature Extraction /
    Tokenization
          ↓
      Model Training
          ↓
       Testing
          ↓
     Evaluation
```

> **Note:** The exact model-wise performance values for the 5-lakh experiment are not included in the information currently provided, so they should not be fabricated. The README should contain the actual Accuracy, Precision, Recall, and F1-score values from your 5-lakh experiment when available.

---

# 📊 RESULTS — 15 LAKH DATASET

The largest reported dataset contains:

# **15 Lakh URLs (~1.5 Million URLs)**

### Sources:

**CommonCrawl + PhishTank**

This experiment focuses on large-scale Machine Learning evaluation.

---

# 🤖 15 Lakh Machine Learning Results

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

# 🏆 Best Model — 15 Lakh

## Random Forest

Random Forest achieved the highest reported performance among the evaluated Machine Learning models.

| Metric        |     Result |
| ------------- | ---------: |
| **Accuracy**  | **95.55%** |
| **Precision** | **95.56%** |
| **Recall**    | **95.26%** |
| **F1-Score**  | **95.41%** |

---

# 🤗 Transformer Results

The reported Transformer comparison includes:

| Model       |   Accuracy |  Precision | Recall |   F1-Score | Training Time |
| ----------- | ---------: | ---------: | -----: | ---------: | ------------: |
| **RoBERTa** | **96.20%** | **96.68%** | 95.49% | **96.08%** |    537.27 sec |
| DistilBERT  |     95.50% |     95.48% | 95.29% |     95.38% |    327.44 sec |
| mBERT       |     93.30% |     92.53% | 93.85% |     93.18% |    812.79 sec |
| TinyBERT    |     92.70% |     92.78% | 92.21% |     92.49% | **62.85 sec** |
| BERT        |     92.80% |     92.44% | 92.83% |     92.63% |    483.50 sec |
| ALBERT      |     92.20% |     90.04% | 94.47% |     92.20% |    392.59 sec |

---

# 🥇 Best Transformer

### **RoBERTa**

RoBERTa achieved:

* **Accuracy:** 96.20%
* **Precision:** 96.68%
* **Recall:** 95.49%
* **F1-Score:** 96.08%

It was the best-performing Transformer in the reported comparison.

---

# ⚡ Fastest Transformer

### **TinyBERT**

TinyBERT achieved the lowest reported training time:

### **62.85 seconds**

This demonstrates that model performance and computational efficiency can involve a trade-off.

---

# 🏆 Overall Results Summary

| Dataset / Experiment | Dataset Size | Source                      | Best Model             |                             Best Result |
| -------------------- | -----------: | --------------------------- | ---------------------- | --------------------------------------: |
| **1.56 Lakh**        |        ~156K | Project dataset             | **1D CNN**             |             **96.76% Testing Accuracy** |
| **1.56 Lakh**        |        ~156K | Project dataset             | **BiLSTM + Attention** |                           **97.45% F1** |
| **1.56 Lakh**        |        ~156K | Project dataset             | **GRU**                |                       **99.09% Recall** |
| **5 Lakh**           |    **~500K** | **CommonCrawl + PhishTank** | —                      | Actual experiment result to be inserted |
| **15 Lakh**          |    **~1.5M** | **CommonCrawl + PhishTank** | **Random Forest**      |                     **95.55% Accuracy** |
| Transformer          |            — | URL-based NLP               | **RoBERTa**            |                     **96.20% Accuracy** |

---

# 📈 Overall Dataset Progression

The complete project can be summarized as:

```text
                  PHISHING URL DETECTION
                           │
                           ▼
                    1.56 LAKH URLs
                           │
                Detailed ML/DL/NLP
                           │
                           ▼
                      5 LAKH URLs
                           │
                  CommonCrawl +
                     PhishTank
                           │
                           ▼
                     15 LAKH URLs
                           │
                  CommonCrawl +
                     PhishTank
                           │
                           ▼
                  LARGE-SCALE STUDY
```

---

# 🔬 Key Findings

### Finding 1 — Strong Deep Learning Performance

The 1.56-lakh experiment showed very strong performance from Deep Learning architectures.

The 1D CNN achieved **96.76% testing accuracy**, while BiLSTM + Attention achieved the highest reported F1-score of **97.45%**.

### Finding 2 — High Recall

GRU achieved **99.09% recall**, demonstrating strong detection of the positive class in the reported experiment.

### Finding 3 — Strong Traditional ML at Large Scale

On the 15-lakh dataset, Random Forest achieved **95.55% accuracy** and **95.41% F1-score**.

### Finding 4 — Transformer Performance

RoBERTa achieved **96.20% accuracy** and **96.08% F1-score** in the reported Transformer comparison.

### Finding 5 — Large-Scale Dataset

The project extends up to **15 lakh URLs**, demonstrating experimentation beyond a small dataset.

### Finding 6 — CommonCrawl + PhishTank

The **5-lakh and 15-lakh datasets specifically use CommonCrawl and PhishTank**, combining web URL data with phishing URL data.

---

# 🛠️ Technologies Used

### Programming Language

* Python

### Data Processing

* Pandas
* NumPy

### Machine Learning

* Scikit-learn
* Random Forest
* Logistic Regression
* Decision Tree
* Naive Bayes
* KNN
* SVC
* AdaBoost
* Voting Classifier

### Boosting

* XGBoost
* LightGBM

### Deep Learning

* ANN
* CNN
* RNN
* LSTM
* GRU
* BiLSTM
* Attention
* Hybrid DL

### NLP / Transformers

* BERT
* RoBERTa
* DistilBERT
* mBERT
* ALBERT
* TinyBERT

---

# 📌 Conclusion

This project presents a comprehensive study of **automated phishing website detection using URL-based Natural Language Processing, Machine Learning, Deep Learning, and Transformer architectures**.

The project evaluates URL classification across multiple scales, beginning with approximately **1.56 lakh URLs**, followed by **5 lakh URLs**, and finally reaching approximately **15 lakh URLs**.

The **5-lakh and 15-lakh datasets were specifically constructed using CommonCrawl and PhishTank**, providing a combination of web URL data and phishing URL data for large-scale experimentation.

The reported results demonstrate strong performance across several model families:

| Area                         | Best Model             |     Result |
| ---------------------------- | ---------------------- | ---------: |
| 1.56 Lakh — Testing Accuracy | **1D CNN**             | **96.76%** |
| 1.56 Lakh — F1-Score         | **BiLSTM + Attention** | **97.45%** |
| 1.56 Lakh — Recall           | **GRU**                | **99.09%** |
| 15 Lakh — ML Accuracy        | **Random Forest**      | **95.55%** |
| Transformer — Accuracy       | **RoBERTa**            | **96.20%** |
| Transformer — F1-Score       | **RoBERTa**            | **96.08%** |

Overall, the project demonstrates that **URL-based patterns can be effectively investigated using Machine Learning, Deep Learning, and NLP techniques**, while the progression from **1.56 lakh → 5 lakh → 15 lakh URLs** provides a strong foundation for studying phishing detection at increasingly large data scales.
