# Automated Detection of Phishing Websites Through URL-Based Natural Language Processing

## 🔐 Project Overview

Phishing is one of the most common cybersecurity threats in which attackers create malicious or deceptive websites and URLs to trick users into revealing sensitive information such as passwords, banking credentials, personal information, and account details.

This project, **“Automated Detection of Phishing Websites Through URL-Based Natural Language Processing,”** focuses on automatically identifying whether a given URL is **legitimate or phishing** by analyzing the characteristics and patterns present in the URL itself.

Instead of relying exclusively on webpage content, the project treats the **URL as a textual/linguistic sequence** and applies a combination of:

* Machine Learning
* Deep Learning
* Natural Language Processing
* Transformer-based architectures
* Ensemble Learning

The project was evaluated at multiple dataset scales, ranging from approximately **1.56 lakh URLs to 15 lakh URLs**.

### Dataset Scale

| Dataset       |   Approximate Size | Data Source / Experiment                   |
| ------------- | -----------------: | ------------------------------------------ |
| **Dataset 1** | **1.56 Lakh URLs** | Detailed ML, DL and Transformer evaluation |
| **Dataset 2** |    **5 Lakh URLs** | **CommonCrawl + PhishTank**                |
| **Dataset 3** |   **15 Lakh URLs** | **CommonCrawl + PhishTank**                |

The use of increasingly larger datasets allows the project to investigate not only classification performance but also the applicability of phishing URL detection at large scale.

---

# 🎯 Problem Statement

Traditional phishing detection systems may rely on blacklists, webpage content, domain reputation, or manually defined rules. However, phishing URLs can change frequently, and newly generated malicious URLs may not yet appear in existing blacklists.

This project therefore investigates a URL-based automated approach where machine learning and NLP models learn patterns directly from URL data.

The central problem addressed is:

> **Can machine learning, deep learning, and Transformer-based NLP models accurately distinguish phishing URLs from legitimate URLs using URL-based information?**

The project further investigates how model performance changes when the amount of available URL data increases from approximately **1.56 lakh to 5 lakh and finally to 15 lakh URLs**.

---

# 💡 Motivation

A URL contains a considerable amount of structural and textual information.

For example:

```text
https://www.example.com/login
```

may exhibit very different characteristics from a suspicious URL containing unusual:

* Characters
* Subdomains
* Paths
* Parameters
* Digits
* Symbols
* Keywords
* URL structures

These patterns can potentially be learned automatically.

The project therefore explores URL classification as a **Natural Language Processing problem**, where URLs can be represented as sequences of characters or tokens and processed using Deep Learning and Transformer architectures.

---

# 🎯 Project Objectives

The major objectives of this project are:

### 1. Automated Phishing URL Detection

Develop an automated system that classifies URLs into phishing and legitimate categories.

### 2. URL-Based Analysis

Analyze the textual and structural characteristics of URLs rather than depending only on webpage content.

### 3. Machine Learning Comparison

Evaluate multiple traditional Machine Learning algorithms and compare their classification performance.

### 4. Deep Learning Analysis

Evaluate sequence-based Deep Learning architectures for learning URL patterns.

### 5. Transformer-Based NLP

Investigate Transformer architectures such as BERT, RoBERTa, DistilBERT, mBERT, ALBERT, and TinyBERT.

### 6. Large-Scale Evaluation

Evaluate the system using:

* **1.56 lakh URLs**
* **5 lakh URLs**
* **15 lakh URLs**

### 7. Performance Evaluation

Compare models using:

* Accuracy
* Precision
* Recall
* F1-Score
* Training Loss
* Testing Loss
* Training Time

where the respective metrics were available.

---

# 🌐 Dataset Sources

## CommonCrawl

The larger datasets use URL data associated with **CommonCrawl**.

CommonCrawl provides large-scale web crawl data and therefore allows the project to work with a very large number of URLs.

---

## PhishTank

The project also uses **PhishTank** as a source of phishing URL data.

The combination of CommonCrawl and PhishTank enables the construction of large URL datasets containing data for phishing detection experiments.

---

# 📊 Dataset Overview

The project consists of three major dataset scales.

| Dataset       |       Size | Source                      | Main Purpose                              |
| ------------- | ---------: | --------------------------- | ----------------------------------------- |
| **1.56 Lakh** |   ~156,000 | Project dataset             | Detailed ML + DL + Transformer comparison |
| **5 Lakh**    |   ~500,000 | **CommonCrawl + PhishTank** | Large-scale evaluation                    |
| **15 Lakh**   | ~1,500,000 | **CommonCrawl + PhishTank** | Very large-scale ML evaluation            |

The progression can be visualized as:

```text
                URL DATA
                   │
       ┌───────────┼───────────┐
       ▼           ▼           ▼
   1.56 LAKH    5 LAKH      15 LAKH
    ~156K        ~500K       ~1.5M
       │           │           │
       ▼           ▼           ▼
   Detailed     Large       Very Large
   Evaluation   Scale       Scale
                Study       Study
```

---

# 📦 Dataset 1 — 1.56 Lakh URLs

The first major experiment contains approximately:

## **1.56 Lakh URLs**

or approximately:

### **156,000 URLs**

This experiment contains the most extensive model comparison in the project.

It evaluates traditional Machine Learning models, Deep Learning models, and Transformer-based models.

---

# 📦 Dataset 2 — 5 Lakh URLs

The second major experiment contains approximately:

## **5 Lakh URLs**

or approximately:

### **500,000 URLs**

### Sources

**CommonCrawl + PhishTank**

The 5-lakh dataset was used to investigate model performance on a significantly larger URL collection.

The dataset construction can be represented as:

```text
                 5 LAKH URL DATASET
                         │
              ┌──────────┴──────────┐
              ▼                     ▼
         CommonCrawl             PhishTank
              │                     │
              ▼                     ▼
        Web URL Data          Phishing URLs
              │                     │
              └──────────┬──────────┘
                         ▼
                  Combined Dataset
                         │
                         ▼
                   ~500,000 URLs
```

---

# 📦 Dataset 3 — 15 Lakh URLs

The largest experiment contains approximately:

## **15 Lakh URLs**

or approximately:

### **1,500,000 URLs**

### Sources

**CommonCrawl + PhishTank**

This experiment extends the evaluation to approximately **1.5 million URLs**, allowing the project to study Machine Learning performance at a substantially larger scale.

---

# 🔄 Complete Project Workflow

```text
                    URL DATA COLLECTION
                            │
             ┌──────────────┴──────────────┐
             ▼                             ▼
        CommonCrawl                    PhishTank
             │                             │
             ▼                             ▼
        Web URL Data                 Phishing URLs
             │                             │
             └──────────────┬──────────────┘
                            ▼
                     DATA PREPARATION
                            │
                            ▼
                    DATA PREPROCESSING
                            │
                            ▼
              FEATURE EXTRACTION /
                    TOKENIZATION
                            │
              ┌─────────────┼─────────────┐
              ▼             ▼             ▼
         Machine         Deep         Transformer
         Learning       Learning          NLP
              │             │             │
              └─────────────┼─────────────┘
                            ▼
                     MODEL TRAINING
                            │
                            ▼
                       PREDICTION
                            │
                            ▼
                       EVALUATION
                            │
              ┌─────────────┼─────────────┐
              ▼             ▼             ▼
          Accuracy      Precision       Recall
                            │
                            ▼
                         F1-Score
```

---

# 🧹 Data Preprocessing

Before applying the classification algorithms, URL data needs to be prepared in a suitable format.

The project pipeline involves processing URLs so that they can be represented appropriately for different model families.

The general processing stages are:

### 1. URL Collection

URLs are collected from the respective datasets.

### 2. Data Cleaning

The collected data is prepared for model training and evaluation.

### 3. Duplicate / Data Handling

Repeated or unsuitable records are handled as part of dataset preparation.

### 4. Class Labelling

URLs are categorized into the corresponding classes.

Conceptually:

```text
Legitimate URL → Legitimate Class
Phishing URL   → Phishing Class
```

### 5. Feature Representation

For traditional ML:

```text
URL
 ↓
URL Features
 ↓
Numerical Representation
```

For Deep Learning and NLP:

```text
URL
 ↓
Tokenization
 ↓
Sequence Representation
```

---

# 🔍 URL Feature Engineering

Traditional Machine Learning algorithms require numerical representations of the input data.

URL-based features can include characteristics such as:

* URL length
* Domain length
* Number of dots
* Number of slashes
* Number of digits
* Number of special characters
* Number of hyphens
* Domain characteristics
* Path characteristics
* Query characteristics
* Lexical patterns

The general pipeline is:

```text
Raw URL
   ↓
Feature Extraction
   ↓
Feature Vector
   ↓
Machine Learning Model
   ↓
Classification
```

---

# 📝 URL Tokenization for NLP

For Deep Learning and Transformer models, URLs can be treated as sequences.

Instead of manually relying only on predefined features, the URL can be represented as a sequence of characters or tokens.

```text
Raw URL
   ↓
Tokenization
   ↓
Token Sequence
   ↓
Embedding / Representation
   ↓
Deep Learning / Transformer
   ↓
Classification
```

This allows sequence-based models to learn patterns from the URL representation.

---

# 🤖 Machine Learning Models

The project evaluates multiple Machine Learning algorithms, including:

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

These models provide a comparison across different machine learning approaches.

---

# 🧠 Deep Learning Models

The project also evaluates several Deep Learning architectures:

* ANN
* RNN
* LSTM
* GRU
* 1D CNN
* BiLSTM + Attention
* Hybrid Deep Learning Model

These models are particularly useful for learning patterns from sequential URL representations.

---

# 🤗 Transformer Models

The Transformer experiments include:

* BERT
* RoBERTa
* DistilBERT
* mBERT
* ALBERT
* TinyBERT

These models are evaluated as NLP-based approaches for URL classification.

---

# 📊 RESULTS — 1.56 LAKH DATASET

The 1.56-lakh dataset experiment provides a detailed comparison across traditional ML, Deep Learning, and Transformer-based approaches.

## Complete Model Performance

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

| Metric                        | Best Model             |     Result |
| ----------------------------- | ---------------------- | ---------: |
| **Highest Training Accuracy** | 1D CNN                 | **97.71%** |
| **Highest Testing Accuracy**  | **1D CNN**             | **96.76%** |
| **Highest Precision**         | 1D CNN                 | **96.02%** |
| **Highest Recall**            | **GRU**                | **99.09%** |
| **Highest F1-Score**          | **BiLSTM + Attention** | **97.45%** |
| **Lowest Testing Loss**       | **Hybrid DL Model**    | **0.1035** |

---

# 🧠 Deep Learning Comparison — 1.56 Lakh

| Model                  | Testing Accuracy |  Precision |     Recall |   F1-Score |
| ---------------------- | ---------------: | ---------: | ---------: | ---------: |
| LSTM                   |           96.52% |     95.84% |     99.02% |     97.41% |
| **1D CNN**             |       **96.76%** | **96.02%** |     98.90% |     97.44% |
| GRU                    |           96.55% |     95.76% | **99.09%** |     97.39% |
| **BiLSTM + Attention** |           96.70% |     95.92% |     99.02% | **97.45%** |
| Transformer            |           93.45% |     92.34% |     98.23% |     95.19% |
| Hybrid DL Model        |           96.66% |     95.88% |     99.02% |     97.42% |

---

# 📊 RESULTS — 5 LAKH DATASET

## Dataset Description

The second large-scale experiment uses:

# **5 Lakh URLs (~500,000 URLs)**

with data from:

### **CommonCrawl + PhishTank**

The experiment evaluates both:

* Traditional Machine Learning
* Transformer-based NLP models

---

# 🤖 Machine Learning Results — 5 Lakh

| Model               |   Accuracy |  Precision |     Recall |   F1-Score |
| ------------------- | ---------: | ---------: | ---------: | ---------: |
| **Random Forest**   | **93.21%** | **93.21%** | **92.75%** | **92.98%** |
| XGBoost             |     91.82% |     91.37% |     91.81% |     91.59% |
| Decision Tree       |     88.43% |     88.36% |     87.69% |     88.02% |
| LightGBM            |     88.02% |     87.14% |     88.35% |     87.74% |
| AdaBoost            |     73.40% |     72.93% |     71.82% |     72.37% |
| Logistic Regression |     66.00% |     66.15% |     61.20% |     63.58% |

---

# 🏆 Best Machine Learning Model — 5 Lakh

### Random Forest

Random Forest achieved the strongest overall performance in the reported 5-lakh Machine Learning experiment.

| Metric        |     Result |
| ------------- | ---------: |
| **Accuracy**  | **93.21%** |
| **Precision** | **93.21%** |
| **Recall**    | **92.75%** |
| **F1-Score**  | **92.98%** |

---

# 🤗 Transformer Results — 5 Lakh

| Model          |   Accuracy |  Precision |     Recall |   F1-Score | Training Time |
| -------------- | ---------: | ---------: | ---------: | ---------: | ------------: |
| BERT           |     91.90% |     88.01% |     95.09% |     91.83% |      461.84 s |
| RoBERTa        |     92.40% |     88.12% | **97.05%** |     92.37% |      638.19 s |
| **DistilBERT** | **92.60%** | **90.00%** |     94.94% | **92.40%** |      324.40 s |
| mBERT          |     90.20% |     84.94% |     96.41% |     90.32% |      561.14 s |
| ALBERT         |     91.50% |     89.45% |     93.04% |     91.21% |      363.08 s |
| TinyBERT       |     90.30% |     85.63% |     95.57% |     90.33% |   **34.69 s** |

---

# 🏆 Best Transformer — 5 Lakh

### DistilBERT

DistilBERT achieved the highest reported accuracy and F1-score among the Transformer models.

| Metric        |     Result |
| ------------- | ---------: |
| **Accuracy**  | **92.60%** |
| **Precision** | **90.00%** |
| **Recall**    | **94.94%** |
| **F1-Score**  | **92.40%** |
| Training Time |   324.40 s |

---

# 🎯 Highest Recall — 5 Lakh

### RoBERTa — **97.05% Recall**

RoBERTa achieved the highest recall among the evaluated Transformer models.

| Metric        |     Result |
| ------------- | ---------: |
| Accuracy      |     92.40% |
| Precision     |     88.12% |
| **Recall**    | **97.05%** |
| F1-Score      |     92.37% |
| Training Time |   638.19 s |

---

# ⚡ Fastest Transformer — 5 Lakh

### TinyBERT — **34.69 Seconds**

TinyBERT recorded the lowest training time among the Transformer models.

| Metric            |      Result |
| ----------------- | ----------: |
| Accuracy          |      90.30% |
| Precision         |      85.63% |
| Recall            |      95.57% |
| F1-Score          |      90.33% |
| **Training Time** | **34.69 s** |

---

# 📊 RESULTS — 15 LAKH DATASET

The largest dataset used in the project contains:

# **15 Lakh URLs (~1.5 Million URLs)**

### Sources

**CommonCrawl + PhishTank**

The 15-lakh experiment focuses on large-scale Machine Learning performance.

---

# 🤖 Machine Learning Results — 15 Lakh

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

Random Forest achieved the highest reported performance in the 15-lakh Machine Learning experiment.

| Metric        | Random Forest Result |
| ------------- | -------------------: |
| **Accuracy**  |           **95.55%** |
| **Precision** |           **95.56%** |
| **Recall**    |           **95.26%** |
| **F1-Score**  |           **95.41%** |

---

# 🤗 Transformer Results — 15 Lakh Experiment

The reported Transformer comparison contains the following models:

| Model       |   Accuracy |  Precision |     Recall |   F1-Score | Training Time |
| ----------- | ---------: | ---------: | ---------: | ---------: | ------------: |
| **BERT**    | **92.80%** |     92.44% |     92.83% |     92.63% |      483.50 s |
| **RoBERTa** | **96.20%** | **96.68%** |     95.49% | **96.08%** |      537.27 s |
| DistilBERT  |     95.50% |     95.48% |     95.29% |     95.38% |      327.44 s |
| mBERT       |     93.30% |     92.53% |     93.85% |     93.18% |      812.79 s |
| ALBERT      |     92.20% |     90.04% | **94.47%** |     92.20% |      392.59 s |
| TinyBERT    |     92.70% |     92.78% |     92.21% |     92.49% |   **62.85 s** |

---

# 🏆 Best Transformer — 15 Lakh Experiment

## RoBERTa

RoBERTa achieved the strongest reported Transformer performance.

| Metric        |     Result |
| ------------- | ---------: |
| **Accuracy**  | **96.20%** |
| **Precision** | **96.68%** |
| Recall        |     95.49% |
| **F1-Score**  | **96.08%** |
| Training Time |   537.27 s |

---

# ⚡ Fastest Transformer — 15 Lakh Experiment

### TinyBERT

TinyBERT recorded the lowest training time:

## **62.85 seconds**

among the reported Transformer models in this experiment.

---

# 🏆 Overall Results Comparison

The complete project results can be summarized as follows:

| Dataset / Experiment    |  Size | Best Model             | Best Metric      |     Result |
| ----------------------- | ----: | ---------------------- | ---------------- | ---------: |
| **1.56 Lakh**           | ~156K | **1D CNN**             | Testing Accuracy | **96.76%** |
| **1.56 Lakh**           | ~156K | **BiLSTM + Attention** | F1-Score         | **97.45%** |
| **1.56 Lakh**           | ~156K | **GRU**                | Recall           | **99.09%** |
| **5 Lakh ML**           | ~500K | **Random Forest**      | Accuracy         | **93.21%** |
| **5 Lakh ML**           | ~500K | **Random Forest**      | F1-Score         | **92.98%** |
| **5 Lakh Transformer**  | ~500K | **DistilBERT**         | Accuracy         | **92.60%** |
| **5 Lakh Transformer**  | ~500K | **DistilBERT**         | F1-Score         | **92.40%** |
| **5 Lakh Transformer**  | ~500K | **RoBERTa**            | Recall           | **97.05%** |
| **15 Lakh ML**          | ~1.5M | **Random Forest**      | Accuracy         | **95.55%** |
| **15 Lakh ML**          | ~1.5M | **Random Forest**      | F1-Score         | **95.41%** |
| **15 Lakh Transformer** | ~1.5M | **RoBERTa**            | Accuracy         | **96.20%** |
| **15 Lakh Transformer** | ~1.5M | **RoBERTa**            | F1-Score         | **96.08%** |

---

# 📈 Dataset Scale Comparison

One of the major aspects of this project is the use of progressively larger datasets.

```text
                       DATASET SCALE
                            │
          ┌─────────────────┼─────────────────┐
          ▼                 ▼                 ▼
      1.56 LAKH          5 LAKH           15 LAKH
       ~156K              ~500K             ~1.5M
          │                 │                 │
          ▼                 ▼                 ▼
      Detailed          Large-Scale       Very Large-
      ML/DL/NLP          ML/NLP             Scale ML
      Evaluation        Evaluation        Evaluation
```

This progression allows the project to study phishing URL detection beyond a single fixed dataset size.

---

# 🏅 Major Findings

## 1. Strong Deep Learning Performance on 1.56 Lakh

The 1.56-lakh experiment showed that Deep Learning models performed strongly.

The **1D CNN achieved 96.76% testing accuracy**, while **BiLSTM + Attention achieved the highest F1-score of 97.45%**.

---

## 2. GRU Achieved Highest Recall on 1.56 Lakh

GRU achieved:

### **99.09% Recall**

This was the highest recall reported in the 1.56-lakh model comparison.

---

## 3. Random Forest Performed Strongly on 5 Lakh

On the 5-lakh CommonCrawl + PhishTank dataset:

### **Random Forest achieved 93.21% accuracy and 92.98% F1-score.**

---

## 4. DistilBERT Performed Best by F1 on 5 Lakh Transformers

Among the reported 5-lakh Transformer models:

### **DistilBERT achieved 92.40% F1-score.**

It also achieved the highest Transformer accuracy:

### **92.60%**

---

## 5. RoBERTa Achieved Highest Recall on 5 Lakh

RoBERTa achieved:

### **97.05% Recall**

among the reported 5-lakh Transformer models.

---

## 6. Random Forest Achieved 95.55% Accuracy on 15 Lakh

On the largest Machine Learning experiment:

### **Random Forest achieved 95.55% accuracy.**

It also achieved:

* **95.56% Precision**
* **95.26% Recall**
* **95.41% F1-Score**

---

## 7. RoBERTa Achieved the Best Transformer Result in the Reported 15-Lakh Comparison

RoBERTa achieved:

### **96.20% Accuracy**

and:

### **96.08% F1-Score**

---

# 🛠️ Technologies Used

## Programming

* Python

## Data Processing

* Pandas
* NumPy

## Machine Learning

* Scikit-learn
* Logistic Regression
* Random Forest
* Decision Tree
* Naive Bayes
* KNN
* Linear SVC
* AdaBoost
* Voting Classifier

## Gradient Boosting

* XGBoost
* LightGBM

## Deep Learning

* ANN
* CNN
* RNN
* LSTM
* GRU
* BiLSTM
* Attention
* Hybrid Deep Learning

## NLP / Transformers

* BERT
* RoBERTa
* DistilBERT
* mBERT
* ALBERT
* TinyBERT



---

# 📊 Performance Evaluation Metrics

## Accuracy

Accuracy measures the overall proportion of correctly classified URLs.

[
Accuracy = \frac{TP + TN}{TP + TN + FP + FN}
]

---

## Precision

Precision measures how many URLs predicted as phishing actually belong to the phishing class.

[
Precision = \frac{TP}{TP + FP}
]

---

## Recall

Recall measures how many actual phishing URLs were correctly detected.

[
Recall = \frac{TP}{TP + FN}
]

For phishing detection, recall is particularly important because failing to detect a phishing URL can expose users to potential attacks.

---

## F1-Score

F1-score provides a balance between Precision and Recall.

[
F1 = 2 \times \frac{Precision \times Recall}{Precision + Recall}
]

---

# 🔬 Conclusion

This project presents a comprehensive investigation of **automated phishing website detection using URL-based Natural Language Processing and Machine Learning techniques**.

The project does not limit the investigation to a single model or a single dataset. Instead, it evaluates multiple model families across progressively larger URL datasets.

The experiments cover approximately:

### **1.56 Lakh → 5 Lakh → 15 Lakh URLs**

The **5-lakh and 15-lakh datasets use CommonCrawl and PhishTank**, enabling large-scale phishing URL experiments.

The reported results demonstrate strong performance across multiple approaches:

* **1D CNN:** 96.76% testing accuracy on the 1.56-lakh experiment
* **BiLSTM + Attention:** 97.45% F1-score on the 1.56-lakh experiment
* **GRU:** 99.09% recall on the 1.56-lakh experiment
* **Random Forest:** 93.21% accuracy on the 5-lakh experiment
* **DistilBERT:** 92.60% accuracy on the 5-lakh Transformer experiment
* **RoBERTa:** 97.05% recall on the 5-lakh Transformer experiment
* **Random Forest:** 95.55% accuracy on the 15-lakh experiment
* **RoBERTa:** 96.20% accuracy on the reported 15-lakh Transformer experiment

Overall, the project demonstrates the potential of **URL-based ML, Deep Learning, and Transformer approaches for automated phishing URL classification**, while the progression from **1.56 lakh to 5 lakh and 15 lakh URLs** provides a broader evaluation of the approaches at different data scales.

---

# Conclusion

This major project, **“Automated Detection of Phishing Websites Through URL-Based Natural Language Processing,”** presents a comprehensive approach for detecting phishing websites by analyzing the textual and structural characteristics of URLs. The primary objective of the project was to develop and evaluate an automated system capable of distinguishing phishing URLs from legitimate URLs using **Machine Learning, Deep Learning, Natural Language Processing, and Transformer-based models**.

A major strength of the project is its evaluation across **multiple dataset sizes**, including approximately **1.56 lakh, 5 lakh, and 15 lakh URLs**. The larger datasets were obtained using **CommonCrawl and PhishTank**, allowing the proposed approaches to be evaluated on increasingly large-scale URL collections rather than relying on a small dataset alone.

The experiments demonstrate that different model architectures have different strengths. On the **1.56-lakh dataset**, Deep Learning models produced particularly strong results, with **1D CNN achieving 96.76% testing accuracy**, while **BiLSTM with Attention achieved the highest F1-score of 97.45%**. GRU achieved a very high recall of **99.09%**, demonstrating its ability to identify a large proportion of phishing URLs.

On the **5-lakh CommonCrawl and PhishTank dataset**, **Random Forest achieved 93.21% accuracy and 92.98% F1-score**, making it the strongest reported traditional Machine Learning model in that experiment. Among the evaluated Transformer models, **DistilBERT achieved 92.60% accuracy and 92.40% F1-score**, while **RoBERTa achieved 97.05% recall**.

The largest experiment, involving approximately **15 lakh URLs**, further demonstrated the capability of the project to work with large-scale data. In this experiment, **Random Forest achieved 95.55% accuracy, 95.56% precision, 95.26% recall, and 95.41% F1-score**. Among the reported Transformer models for this experiment, **RoBERTa achieved 96.20% accuracy and 96.08% F1-score**, showing strong performance on the large URL dataset.

Overall, the project demonstrates that **URL-based analysis can provide an effective foundation for automated phishing detection**. The comparison of traditional Machine Learning, Deep Learning, and Transformer architectures provides valuable insight into the strengths and trade-offs of different approaches. The results also show that increasing the dataset scale enables the system to be evaluated under more realistic large-scale conditions.

The project successfully combines **cybersecurity, Natural Language Processing, Machine Learning, and Deep Learning** into a unified phishing detection framework. The work establishes a strong foundation for future development of more scalable and intelligent phishing detection systems. Future extensions can focus on improving generalization to newly emerging phishing URLs, incorporating additional URL and domain-level information, optimizing computational requirements, and developing real-time deployment mechanisms.

### **In conclusion, this major project demonstrates the feasibility of building an automated and data-driven phishing URL detection system and provides a detailed comparative evaluation of multiple ML, DL, and Transformer-based approaches across datasets ranging from 1.56 lakh to 15 lakh URLs.**


