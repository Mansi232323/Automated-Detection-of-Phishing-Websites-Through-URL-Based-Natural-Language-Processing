Yes. I’ll rewrite the **README completely from the beginning**, in a detailed, professional GitHub format, while keeping your actual project information and reported results. I’ll also include the **ML and Transformer tables from your screenshot** in the Results section. The project scope, datasets, models, workflow, metrics, and existing findings are supported by your uploaded README. 

# 🔐 Automated Detection of Phishing Websites Through URL-Based Natural Language Processing

> **An end-to-end Machine Learning, Deep Learning, and Transformer-based cybersecurity framework for automated phishing URL detection.**

Phishing websites are one of the most common and dangerous cybersecurity threats. Attackers frequently create malicious websites and URLs designed to steal sensitive information such as **usernames, passwords, banking credentials, credit card information, personal data, and authentication details**.

Traditional phishing detection systems often depend heavily on blacklists and previously reported malicious URLs. Although blacklist-based approaches can be effective for known threats, they may struggle when attackers generate **new, modified, or previously unseen phishing URLs**.

This project presents an **automated phishing URL detection framework** that analyzes URLs directly and applies multiple Artificial Intelligence approaches to determine whether a URL is **legitimate or phishing**.

The project benchmarks several generations of AI techniques, including:

* Traditional Machine Learning
* Deep Learning
* Sequence-based Neural Networks
* Hybrid Deep Learning
* Transformer-based Natural Language Processing

The models are evaluated using multiple performance metrics, including:

* Accuracy
* Precision
* Recall
* F1-Score
* Training Loss
* Validation Loss
* Training Time

The project experiments with large-scale URL datasets collected from sources including **Kaggle, Common Crawl, and PhishTank**, with experiments involving approximately **5 lakh and 15 lakh URL records**. 

---

# 📌 Table of Contents

* [Project Overview](#-project-overview)
* [Problem Statement](#-problem-statement)
* [Why Phishing URL Detection?](#-why-phishing-url-detection)
* [Objectives](#-objectives)
* [Key Features](#-key-features)
* [Dataset](#-dataset)
* [Data Sources](#-data-sources)
* [Data Processing Pipeline](#-data-processing-pipeline)
* [Feature Engineering](#-feature-engineering)
* [URL Representation](#-url-representation)
* [Models Implemented](#-models-implemented)
* [Machine Learning Models](#-machine-learning-models)
* [Deep Learning Models](#-deep-learning-models)
* [Hybrid CNN + LSTM](#-hybrid-cnn--lstm)
* [Transformer Models](#-transformer-models)
* [Machine Learning Results](#-machine-learning-results)
* [Detailed ML Analysis](#-detailed-ml-analysis)
* [Transformer Results](#-transformer-results)
* [Detailed Transformer Analysis](#-detailed-transformer-analysis)
* [Training vs Testing Performance](#-training-vs-testing-performance)
* [Comprehensive Model Benchmark](#-comprehensive-model-benchmark)
* [Overall Model Comparison](#-overall-model-comparison)
* [Evaluation Metrics](#-evaluation-metrics)
* [Project Workflow](#-project-workflow)
* [Technologies Used](#-technologies-used)
* [Repository Structure](#-repository-structure)
* [Visual Analysis](#-visual-analysis)
* [Key Findings](#-key-findings)
* [Performance vs Computational Cost](#-performance-vs-computational-cost)
* [Potential Applications](#-potential-applications)
* [Future Improvements](#-future-improvements)
* [Experimental Limitations](#-experimental-limitations)
* [Security Disclaimer](#-security-disclaimer)
* [Conclusion](#-conclusion)
* [Author](#-author)

---

# 🔎 Project Overview

The main objective of this project is to investigate how effectively Artificial Intelligence techniques can detect phishing websites by analyzing **URL-level information**.

Instead of depending entirely on previously reported malicious websites, the proposed approach learns patterns directly from URL data.

A URL contains several potentially useful signals, including:

* URL length
* Domain structure
* Number of subdirectories
* Special characters
* Digits
* Hyphens
* Dots
* Query parameters
* Suspicious keywords
* IP addresses
* Character-level patterns
* Token-level patterns
* URL entropy
* Other lexical and structural characteristics

These characteristics can help Machine Learning and Deep Learning models identify patterns associated with phishing URLs.

The project evaluates four major categories of AI approaches:

### 1️⃣ Traditional Machine Learning

* Linear Regression
* Logistic Regression
* Random Forest
* Linear SVC
* KNN
* Gaussian Naive Bayes
* Decision Tree
* AdaBoost
* LightGBM
* XGBoost
* Voting Classifier

### 2️⃣ Deep Learning

* ANN / DNN
* RNN
* LSTM
* GRU
* 1D CNN
* BiLSTM + Attention

### 3️⃣ Hybrid Deep Learning

* CNN + LSTM Hybrid Architecture

### 4️⃣ Transformer-Based NLP

* BERT
* RoBERTa
* DistilBERT
* mBERT
* ALBERT
* TinyBERT

These experiments allow the project to compare different generations of AI models for the same cybersecurity problem. 

---

# 🚨 Problem Statement

Phishing attacks continuously evolve.

Attackers can create:

* Newly registered domains
* Look-alike domains
* URL redirects
* Fake login pages
* Suspicious subdomains
* Malicious query parameters
* Obfuscated URLs
* URLs containing misleading keywords

A URL may therefore be malicious even when it has not previously appeared in a blacklist.

A robust phishing detection system should be able to:

1. Detect previously unseen malicious URLs.
2. Learn URL-level linguistic and structural patterns.
3. Process large-scale datasets efficiently.
4. Maintain high recall.
5. Maintain high precision.
6. Minimize false negatives.
7. Compare traditional ML with modern Deep Learning and Transformer approaches.
8. Provide a foundation for real-time cybersecurity applications.

The project's objective is therefore not simply to achieve high accuracy, but to investigate which AI approaches provide the most useful balance of **accuracy, precision, recall, F1-score, and computational cost**. 

---

# 💡 Why Phishing URL Detection?

Traditional blacklist-based detection can be represented as:

```text
                  New URL
                     │
                     ▼
              ┌─────────────┐
              │   Blacklist │
              └──────┬──────┘
                     │
              ┌──────┴──────┐
              │             │
             YES            NO
              │             │
              ▼             ▼
           BLOCK          ALLOW
```

The major limitation is that a newly generated phishing URL may not yet exist in the blacklist.

The proposed approach instead learns characteristics from URLs:

```text
                   New URL
                      │
                      ▼
              URL Representation
                      │
                      ▼
             ML / DL / Transformer
                      │
                      ▼
             Learned URL Patterns
                      │
                      ▼
             Phishing Probability
                      │
              ┌───────┴───────┐
              ▼               ▼
          Phishing         Legitimate
```

This provides a more adaptive approach to detecting previously unseen phishing patterns. 

---

# 🎯 Objectives

The major objectives of this project are:

* Build an automated phishing URL classification system.
* Process large-scale phishing and legitimate URL datasets.
* Perform URL preprocessing and cleaning.
* Extract meaningful URL features.
* Apply NLP-based URL representation.
* Benchmark traditional Machine Learning algorithms.
* Evaluate Deep Learning architectures.
* Investigate sequence-based neural networks.
* Implement a hybrid CNN-LSTM architecture.
* Evaluate Transformer models for URL classification.
* Compare models using Accuracy, Precision, Recall, and F1-Score.
* Analyze training and validation behavior.
* Compare model performance with computational cost.
* Identify suitable models for practical phishing detection. 

---

# ✨ Key Features

The project provides the following capabilities:

* 🔐 Automated phishing URL detection
* 📊 Large-scale URL dataset experimentation
* 🧹 URL preprocessing and cleaning
* 🔤 URL tokenization
* 🧠 Traditional Machine Learning
* 🤖 Deep Learning
* 🔄 Sequence modeling
* 🧬 Hybrid CNN-LSTM architecture
* 🤗 Transformer-based NLP
* 📈 Accuracy evaluation
* 🎯 Precision evaluation
* 🔍 Recall evaluation
* 📊 F1-score evaluation
* 📉 Training and validation loss analysis
* ⏱️ Training-time comparison
* 📊 Comparative model benchmarking
* ⚡ Scalable experimentation
* 🔎 Performance analysis across multiple AI paradigms

---

# 📂 Dataset

The project uses phishing and legitimate URL data collected from multiple sources.

The experiments include datasets of different scales, including approximately:

* **5 Lakh URLs**
* **15 Lakh URLs**

The larger datasets allow the project to investigate how different models behave when trained on significantly larger amounts of URL information.

---

# 🌐 Data Sources

| Source                | Purpose                             |
| --------------------- | ----------------------------------- |
| **Kaggle**            | Phishing and legitimate URL samples |
| **PhishTank**         | Known phishing URLs                 |
| **Common Crawl**      | Large-scale web URL collection      |
| **Combined Datasets** | Expanded training and evaluation    |

The combination of multiple sources provides a broader range of URL patterns for model training and evaluation. 

---

# 🧹 Data Processing Pipeline

The overall data-processing pipeline follows the sequence below:

```text
Raw URL Dataset
       │
       ▼
Data Collection
       │
       ▼
Data Cleaning
       │
       ▼
Duplicate Removal
       │
       ▼
Missing / Invalid URL Handling
       │
       ▼
URL Normalization
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
Prediction
       │
       ▼
Performance Evaluation
       │
       ▼
Model Comparison
```

The purpose of preprocessing is to transform raw URL data into a representation suitable for Machine Learning, Deep Learning, and Transformer models. 

---

# 🔤 Feature Engineering

Traditional Machine Learning models use URL-based structural and lexical features.

Potential URL features include:

| Feature                | Description                              |
| ---------------------- | ---------------------------------------- |
| URL Length             | Total number of characters in the URL    |
| Number of Dots         | Number of `.` characters                 |
| Number of Hyphens      | Number of `-` characters                 |
| Special Characters     | Count of suspicious/special symbols      |
| Number of Digits       | Number of numerical characters           |
| Subdirectories         | Number of path levels                    |
| Query Parameters       | Number of parameters in the URL          |
| IP Address             | Whether an IP address appears in the URL |
| HTTPS                  | Whether HTTPS is present                 |
| Suspicious Keywords    | Presence of phishing-related terms       |
| Domain Characteristics | Structural properties of the domain      |
| Character Frequency    | Frequency distribution of characters     |
| URL Entropy            | Measure of randomness in the URL         |

These features allow traditional Machine Learning models to learn structural differences between legitimate and phishing URLs. 

---

# 🔤 URL Representation for NLP Models

Deep Learning and Transformer models can treat URLs as sequences.

For example:

```text
https://secure-login-example.com/verify/account
```

can be represented as a sequence of characters or tokens.

Important patterns may include:

```text
secure
login
verify
account
-
/
@
?
=
```

The model can learn combinations of these patterns that may be associated with malicious URLs. 

---

# 🤖 Models Implemented

The project investigates multiple categories of AI models.

---

## 1. Traditional Machine Learning

The following models are evaluated:

1. Linear Regression
2. Logistic Regression
3. Random Forest
4. Linear SVC
5. KNN
6. Gaussian Naive Bayes
7. Decision Tree
8. AdaBoost
9. LightGBM
10. XGBoost
11. Voting Classifier

---

## 2. Deep Learning

The project evaluates:

* ANN / DNN
* RNN
* LSTM
* GRU
* 1D CNN
* BiLSTM + Attention

These models investigate whether neural architectures can learn character-level and sequence-level URL patterns. 

---

# 🧠 Deep Learning Architectures

## ANN / DNN

Artificial Neural Networks provide baseline deep-learning architectures based primarily on fully connected layers.

They can learn nonlinear relationships between extracted URL representations and phishing labels.

---

## 🔄 RNN

Recurrent Neural Networks are designed to process sequential information.

For URL classification, an RNN can process URL characters or tokens sequentially and attempt to learn dependencies between different parts of the URL.

---

## 🧠 LSTM

Long Short-Term Memory networks are designed to capture longer-term dependencies in sequential data.

For URLs, this can help model relationships between different characters or tokens that occur at different positions.

---

## ⚡ GRU

Gated Recurrent Units provide another recurrent architecture.

GRU can capture sequential URL patterns while generally using a simpler recurrent structure than LSTM.

---

## 🧩 1D CNN

A one-dimensional Convolutional Neural Network can detect local patterns within URL sequences.

For example, it can learn patterns involving:

```text
login
verify
secure
account
admin
```

as well as combinations of special characters and URL structures.

---

## 👀 BiLSTM + Attention

BiLSTM processes URL sequences in both directions.

The attention mechanism can help the model focus on important regions of the URL rather than treating every portion equally.

The project reports strong performance from this architecture in the comprehensive benchmark. 

---

# 🧬 Hybrid CNN + LSTM

The hybrid architecture combines the strengths of CNN and LSTM.

```text
                 URL Input
                    │
                    ▼
          Embedding / Representation
                    │
           ┌────────┴────────┐
           ▼                 ▼
         1D CNN             LSTM
           │                 │
           └────────┬────────┘
                    ▼
              Feature Fusion
                    │
                    ▼
               Dense Layers
                    │
                    ▼
              Classification
```

The purpose of the architecture is to combine:

* **CNN** → local URL pattern extraction
* **LSTM** → sequential dependency learning

The reported hybrid experiment achieved:

| Metric            |  Score |
| ----------------- | -----: |
| Training Accuracy | 55.94% |
| Testing Accuracy  | 56.36% |
| Training Loss     | 0.6745 |
| Testing Loss      | 0.6712 |

The relatively low result demonstrates that increasing architectural complexity does not automatically guarantee better performance. Feature representation, architecture design, training configuration, and hyperparameter selection remain critical. 

---

# 🤗 Transformer Models

The project evaluates six Transformer-based architectures:

* BERT
* RoBERTa
* DistilBERT
* mBERT
* ALBERT
* TinyBERT

These models investigate whether pretrained language representations can effectively capture the linguistic and structural characteristics of URLs. 

---

# 📊 Machine Learning Results

The following results are from the **Machine Learning experiment shown in the project results**.

| Rank | Model               |   Accuracy |  Precision |     Recall |   F1-Score |
| ---: | ------------------- | ---------: | ---------: | ---------: | ---------: |
|   🥇 | **Random Forest**   | **95.55%** | **95.56%** | **95.26%** | **95.41%** |
|   🥈 | XGBoost             |     92.29% |     91.91% |     92.22% |     92.07% |
|   🥉 | Decision Tree       |     91.54% |     91.46% |     91.07% |     91.26% |
|    4 | LightGBM            |     88.13% |     87.37% |     88.28% |     87.83% |
|    5 | Hybrid Ensemble     |     78.24% |     87.00% |     64.82% |     74.29% |
|    6 | AdaBoost            |     72.78% |     73.38% |     68.86% |     71.05% |
|    7 | Logistic Regression |     65.73% |     65.90% |     60.77% |     63.23% |
|    8 | Linear Regression   |     65.59% |     65.94% |     60.11% |     62.89% |
|    9 | Naive Bayes         |     56.72% |     65.89% |     22.30% |     33.32% |

---

# 🏆 Best Machine Learning Model — Random Forest

Random Forest achieved the strongest overall performance in the reported Machine Learning experiment.

### Performance

| Metric        | Random Forest |
| ------------- | ------------: |
| **Accuracy**  |    **95.55%** |
| **Precision** |    **95.56%** |
| **Recall**    |    **95.26%** |
| **F1-Score**  |    **95.41%** |

Random Forest achieved more than **95% across all four primary classification metrics**.

This is particularly important because it indicates that the model does not simply achieve high accuracy while sacrificing precision or recall.

Instead, the four metrics remain relatively balanced.

---

# 🔍 Detailed Machine Learning Analysis

## 🌲 Random Forest

Random Forest was the strongest traditional ML model.

Its high recall indicates strong capability in identifying phishing URLs, while its high precision indicates relatively few false phishing predictions.

The combination of:

**95.55% Accuracy + 95.56% Precision + 95.26% Recall + 95.41% F1**

makes Random Forest a strong baseline for the project.

---

## 🚀 XGBoost

XGBoost achieved:

* **92.29% Accuracy**
* **91.91% Precision**
* **92.22% Recall**
* **92.07% F1-Score**

The model produced a strong balance between precision and recall.

Its recall of **92.22%** indicates that it detected a large proportion of phishing URLs.

---

## 🌳 Decision Tree

Decision Tree achieved:

* **91.54% Accuracy**
* **91.46% Precision**
* **91.07% Recall**
* **91.26% F1-Score**

The results show that even a single tree can learn useful phishing-related patterns from the URL features.

However, Random Forest improved performance considerably by using an ensemble of decision trees.

---

## 💡 LightGBM

LightGBM achieved:

* **88.13% Accuracy**
* **87.37% Precision**
* **88.28% Recall**
* **87.83% F1-Score**

The model provides reasonably balanced classification performance but remains below Random Forest and XGBoost in this experiment.

---

## ⚡ AdaBoost

AdaBoost achieved:

* **72.78% Accuracy**
* **73.38% Precision**
* **68.86% Recall**
* **71.05% F1-Score**

Its performance is considerably lower than the strongest tree-based models.

---

## 📉 Logistic Regression

Logistic Regression achieved:

* **65.73% Accuracy**
* **65.90% Precision**
* **60.77% Recall**
* **63.23% F1-Score**

This indicates that the URL classification patterns were not captured as effectively by this baseline model as by the ensemble tree-based approaches.

---

## 📉 Linear Regression

Linear Regression achieved:

* **65.59% Accuracy**
* **65.94% Precision**
* **60.11% Recall**
* **62.89% F1-Score**

Its performance was similar to Logistic Regression but remained significantly below Random Forest.

---

## ⚠️ Naive Bayes

Naive Bayes achieved:

* **56.72% Accuracy**
* **65.89% Precision**
* **22.30% Recall**
* **33.32% F1-Score**

The major weakness is recall.

A recall of **22.30%** means that the model failed to detect a substantial proportion of phishing URLs in this experiment.

For a cybersecurity application, this is a significant limitation.

---

# 🤗 Transformer Results

The Transformer experiment produced the following results:

| Rank | Model          |   Accuracy |   Precision |      Recall |    F1-Score | Training Time |
| ---: | -------------- | ---------: | ----------: | ----------: | ----------: | ------------: |
|   🥇 | **RoBERTa**    | **96.20%** | **96.681%** |     95.492% | **96.083%** |      537.27 s |
|   🥈 | **DistilBERT** | **95.50%** |     95.483% |     95.269% |     95.385% |      327.44 s |
|   🥉 | mBERT          |     93.30% |     92.525% |     93.853% |     93.184% |      812.28 s |
|    4 | TinyBERT       |     92.70% |     92.874% |     92.213% |     92.497% |   **62.85 s** |
|    5 | BERT           |     92.80% |     92.449% |     92.828% |     92.638% |      483.50 s |
|    6 | ALBERT         |     92.20% |     90.039% | **94.467%** |     92.200% |      392.58 s |

---

# 🏆 Best Transformer Model — RoBERTa

RoBERTa achieved the strongest overall Transformer performance.

| Metric        |        RoBERTa |
| ------------- | -------------: |
| **Accuracy**  |     **96.20%** |
| **Precision** |    **96.681%** |
| **Recall**    |    **95.492%** |
| **F1-Score**  |    **96.083%** |
| Training Time | 537.27 seconds |

RoBERTa achieved the highest reported:

* Accuracy
* Precision
* F1-Score

among the evaluated Transformer models.

Its recall also exceeded 95%, which is highly relevant for phishing detection.

---

# 🥈 DistilBERT

DistilBERT achieved:

| Metric        |        Score |
| ------------- | -----------: |
| Accuracy      |   **95.50%** |
| Precision     |  **95.483%** |
| Recall        |  **95.269%** |
| F1-Score      |  **95.385%** |
| Training Time | **327.44 s** |

DistilBERT is particularly interesting because its performance is close to RoBERTa while requiring less training time in the reported experiment.

---

# 🌍 mBERT

mBERT achieved:

| Metric        |    Score |
| ------------- | -------: |
| Accuracy      |   93.30% |
| Precision     |  92.525% |
| Recall        |  93.853% |
| F1-Score      |  93.184% |
| Training Time | 812.28 s |

mBERT achieved strong recall but had the highest reported training time.

---

# 🧠 ALBERT

ALBERT achieved:

| Metric        |       Score |
| ------------- | ----------: |
| Accuracy      |      92.20% |
| Precision     |     90.039% |
| **Recall**    | **94.467%** |
| F1-Score      |     92.200% |
| Training Time |    392.58 s |

ALBERT's strongest characteristic in this experiment was recall.

Its **94.467% recall** demonstrates strong capability in identifying phishing URLs.

---

# ⚡ TinyBERT

TinyBERT achieved:

| Metric            |       Score |
| ----------------- | ----------: |
| Accuracy          |      92.70% |
| Precision         |     92.874% |
| Recall            |     92.213% |
| F1-Score          |     92.497% |
| **Training Time** | **62.85 s** |

TinyBERT had the **lowest training time** among all reported Transformer models.

This makes it an attractive option for applications where computational efficiency is more important than achieving the absolute highest classification score.

---

# 📊 Transformer Training-Time Comparison

| Model        | Training Time |
| ------------ | ------------: |
| **TinyBERT** |   **62.85 s** |
| DistilBERT   |      327.44 s |
| ALBERT       |      392.58 s |
| BERT         |      483.50 s |
| RoBERTa      |      537.27 s |
| mBERT        |      812.28 s |

The difference between TinyBERT and mBERT demonstrates the importance of computational efficiency when selecting a Transformer architecture.

---

# 🧠 Training vs Testing Performance

The project also evaluates the relationship between training and testing performance.

## 1D CNN

| Metric    | Training | Testing |
| --------- | -------: | ------: |
| Loss      |   0.2531 |  0.2731 |
| Accuracy  |   89.52% |  88.34% |
| Precision |   87.85% |  86.47% |
| Recall    |   90.83% |  90.05% |
| F1-Score  |   89.32% |  88.22% |

The relatively small difference between training and testing metrics indicates reasonably consistent performance.

---

## GRU

| Metric    | Training |    Testing |
| --------- | -------: | ---------: |
| Loss      |   0.2533 |     0.2627 |
| Accuracy  |   89.86% | **89.43%** |
| Precision |   88.29% |     87.72% |
| Recall    |   91.04% | **90.93%** |
| F1-Score  |   89.64% | **89.30%** |

GRU produced strong testing recall and F1-score in this experiment.

---

## DNN

| Metric    | Training | Testing |
| --------- | -------: | ------: |
| Loss      |   0.2675 |  0.3021 |
| Accuracy  |   89.00% |  87.05% |
| Precision |   88.61% |  86.45% |
| Recall    |   88.58% |  86.92% |
| F1-Score  |   88.60% |  86.69% |

The DNN showed a larger training-to-testing reduction than the 1D CNN and GRU experiments.

---

# 📊 Comprehensive Model Benchmark

A separate comprehensive experiment compared traditional Machine Learning and Deep Learning models.

| Model               | Training Accuracy | Testing Accuracy | Precision |     Recall |   F1-Score |
| ------------------- | ----------------: | ---------------: | --------: | ---------: | ---------: |
| Logistic Regression |            77.29% |           77.30% |    77.32% |     96.64% |     85.91% |
| Random Forest       |            88.07% |           85.63% |    86.45% |     94.80% |     90.43% |
| Linear SVC          |            77.21% |           77.27% |    76.90% |     97.57% |     86.01% |
| KNN                 |            87.57% |           83.05% |    85.85% |     91.39% |     88.53% |
| Gaussian NB         |            75.71% |           76.56% |    77.04% |     95.81% |     85.41% |
| Decision Tree       |            86.97% |           85.02% |    86.36% |     93.92% |     89.98% |
| AdaBoost            |            77.66% |           77.72% |    77.65% |     96.72% |     86.14% |
| LightGBM            |            84.36% |           84.26% |    84.31% |     95.86% |     89.72% |
| XGBoost             |            85.01% |           84.84% |    84.91% |     95.85% |     90.05% |
| Voting Classifier   |            84.47% |           84.36% |    83.41% |     97.55% |     89.93% |
| ANN                 |            83.78% |           83.76% |    83.29% |     93.88% |     88.24% |
| RNN                 |            75.42% |           75.49% |    73.03% |     98.59% |     83.85% |
| LSTM                |            97.48% |           96.52% |    95.84% |     99.02% |     97.41% |
| **1D CNN**          |            97.71% |       **96.76%** |    96.02% |     98.90% | **97.44%** |
| GRU                 |            97.53% |           96.55% |    95.76% | **99.09%** |     97.39% |
| BiLSTM + Attention  |            97.60% |           96.70% |    95.92% |     99.02% | **97.45%** |
| Transformer         |            93.78% |           93.45% |    92.34% |     98.23% |     95.19% |
| Hybrid DL Model     |            97.64% |           96.66% |    95.88% |     99.02% |     97.42% |

This separate benchmark reports very strong performance from sequence-based Deep Learning architectures.

### 🏆 Highest Testing Accuracy

**1D CNN — 96.76%**

### 🏆 Highest F1-Score

**BiLSTM + Attention — 97.45%**

### 🏆 Highest Recall

**GRU — 99.09%**

These results demonstrate the effectiveness of neural sequence architectures for learning URL-level patterns. 

> **Important:** This is a separate comprehensive experiment with its own preprocessing and feature configuration. Therefore, these values should not automatically be treated as directly comparable to the ML and Transformer results above.

---

# 🏅 Best Performing Models Across Experiments

## 🥇 1D CNN

In the comprehensive benchmark:

* Testing Accuracy: **96.76%**
* F1-Score: **97.44%**

1D CNN effectively captures local character-level patterns within URLs.

---

## 🥈 BiLSTM + Attention

The comprehensive benchmark reports:

* Testing Accuracy: **96.70%**
* F1-Score: **97.45%**

The attention mechanism allows the architecture to focus on important regions of the URL sequence.

---

## 🥉 Hybrid Deep Learning

The Hybrid DL model achieved:

* Testing Accuracy: **96.66%**
* F1-Score: **97.42%**

This demonstrates the potential of combining multiple representation-learning approaches.

---

# 📐 Evaluation Metrics

The project uses four primary classification metrics.

---

## Accuracy

Accuracy measures the proportion of correctly classified URLs.

```text
Accuracy = Correct Predictions / Total Predictions
```

A high accuracy indicates that the model correctly classifies a large proportion of the total URLs.

---

## Precision

Precision measures how many URLs predicted as phishing were actually phishing.

```text
Precision = TP / (TP + FP)
```

High precision helps reduce false phishing warnings.

---

## Recall

Recall measures how many actual phishing URLs were successfully detected.

```text
Recall = TP / (TP + FN)
```

Recall is particularly important in cybersecurity because missing a phishing URL can have serious consequences.

---

## F1-Score

F1-score is the harmonic mean of Precision and Recall.

```text
F1 = 2 × (Precision × Recall) / (Precision + Recall)
```

F1-score is useful when both false positives and false negatives matter. 

---

# 🔄 Project Workflow

```text
                     ┌─────────────────────┐
                     │   URL Data Sources  │
                     │ Kaggle / PhishTank  │
                     │    Common Crawl     │
                     └──────────┬──────────┘
                                │
                                ▼
                     ┌─────────────────────┐
                     │ Data Cleaning       │
                     │ Duplicate Removal   │
                     │ URL Normalization   │
                     └──────────┬──────────┘
                                │
                                ▼
                     ┌─────────────────────┐
                     │ Feature Engineering │
                     │ / Tokenization      │
                     └──────────┬──────────┘
                                │
             ┌──────────────────┼──────────────────┐
             ▼                  ▼                  ▼
      Machine Learning    Deep Learning       Transformers
             │                  │                  │
             ▼                  ▼                  ▼
       RF / XGBoost       CNN / LSTM / GRU   BERT / RoBERTa
       LightGBM etc.      BiLSTM / DNN       DistilBERT etc.
             │                  │                  │
             └──────────────────┼──────────────────┘
                                │
                                ▼
                     ┌─────────────────────┐
                     │ Model Evaluation    │
                     │ Accuracy            │
                     │ Precision           │
                     │ Recall              │
                     │ F1-Score            │
                     │ Training Time       │
                     └──────────┬──────────┘
                                │
                                ▼
                     ┌─────────────────────┐
                     │ Model Comparison    │
                     └─────────────────────┘
```

---

# 🛠️ Technologies Used

## Programming Language

* Python

## Data Processing

* Pandas
* NumPy

## Visualization

* Matplotlib
* Seaborn

## Machine Learning

* Scikit-learn
* Random Forest
* XGBoost
* LightGBM
* AdaBoost

## Deep Learning

* TensorFlow
* Keras

## NLP / Transformers

* Hugging Face Transformers
* Tokenizers

## Development Environment

* Jupyter Notebook
* Google Colab
* GitHub

These technologies form the complete experimentation stack used throughout the project. 

---

# 📁 Repository Structure

```text
Automated-Detection-of-Phishing-Websites-Through-URL-Based-Natural-Language-Processing/
│
├── 15_lakh_dataset_(CommonCrawl_and_PhishTank...)
│
├── 15lakh_dataset_(commoncrawl_and_phishing...)
│
├── 5Lakh_DL_Common_Crawl_&_PhishTank.ipynb
│
├── 5Lakh_ML_Common_Crawl_&_PhishTank.ipynb
│
├── MY_kaggle.ipynb
│
├── README.md
│
└── assets/
    ├── ml-results.png
    ├── dl-results.png
    ├── transformer-results.png
    └── model-comparison.png
```

---

# 📊 Visual Analysis

The project includes comparative visualizations for:

* Model Accuracy
* Precision
* Recall
* F1-Score
* Training Loss
* Validation Loss
* Training vs Testing Accuracy
* Transformer Training Time
* Model-wise performance comparison

A grouped comparison can be represented as:

```text
Accuracy
Precision
Recall
F1-Score
```

across the evaluated models.

These visualizations make it easier to identify the strongest models and understand the differences between Machine Learning, Deep Learning, and Transformer approaches. 

---

# 🔍 Key Findings

## 1. Ensemble Machine Learning Models Are Strong Baselines

Random Forest achieved approximately **95.55% accuracy** in the reported ML experiment.

This demonstrates that traditional Machine Learning can be highly effective for URL-based phishing detection.

---

## 2. Random Forest Is the Best Reported Traditional ML Model

Random Forest achieved:

**95.55% Accuracy**

**95.56% Precision**

**95.26% Recall**

**95.41% F1-Score**

making it the strongest ML model in the reported result table.

---

## 3. RoBERTa Is the Strongest Reported Transformer

RoBERTa achieved:

**96.20% Accuracy**

**96.681% Precision**

**95.492% Recall**

**96.083% F1-Score**

making it the strongest Transformer model in the provided results.

---

## 4. Deep Learning Can Learn URL Patterns

CNN and recurrent architectures can learn character- and sequence-level patterns that may not be captured as effectively through simple manually engineered features.

---

## 5. 1D CNN Performs Extremely Well in the Separate Comprehensive Benchmark

The comprehensive benchmark reports:

**96.76% Testing Accuracy**

and

**97.44% F1-Score**

for 1D CNN.

---

## 6. BiLSTM + Attention Achieves a Strong F1-Score

The comprehensive benchmark reports:

**97.45% F1-Score**

for BiLSTM + Attention.

---

## 7. GRU Achieves Very High Recall

The comprehensive benchmark reports:

**99.09% Recall**

for GRU.

This is particularly significant for phishing detection because recall is directly related to the ability to detect actual phishing URLs.

---

## 8. Transformer Models Provide Strong Performance

RoBERTa and DistilBERT demonstrate that Transformer-based URL representations can achieve competitive classification results.

---

## 9. TinyBERT Provides Computational Efficiency

TinyBERT achieved the lowest reported Transformer training time:

**62.85 seconds**

---

## 10. Complex Architecture Does Not Automatically Guarantee Better Results

The reported CNN + LSTM experiment achieved only approximately:

**56.36% Testing Accuracy**

This demonstrates that architecture complexity alone does not guarantee improved performance.

Effective feature representation, preprocessing, optimization, and architecture design remain essential.

---

# ⚖️ Performance vs Computational Cost

A real-world phishing detection system must balance performance with computational requirements.

Important considerations include:

* Detection accuracy
* Precision
* Recall
* F1-score
* Training time
* Inference latency
* Model size
* Memory requirements
* Hardware requirements
* Scalability
* False-negative rate

For example:

| Requirement                                    | Recommended Model               |
| ---------------------------------------------- | ------------------------------- |
| Highest reported Transformer performance       | **RoBERTa**                     |
| Best traditional ML performance                | **Random Forest**               |
| Fastest Transformer training                   | **TinyBERT**                    |
| Strong performance with lower Transformer cost | **DistilBERT**                  |
| Strong sequence-model benchmark                | **1D CNN / BiLSTM + Attention** |

The final model selection should therefore depend on the intended deployment environment rather than accuracy alone. 

---

# 🌐 Potential Applications

The proposed phishing detection framework can potentially be adapted for:

* 🏦 Banking security
* 💳 Online payment protection
* 📧 Email security systems
* 🌐 Web browsers
* 🛡️ Security Operations Centers
* 🔐 Enterprise cybersecurity
* 📱 Mobile security applications
* 🎣 Anti-phishing browser extensions
* 🔎 Threat intelligence platforms
* 🚨 Real-time URL screening systems

These applications can use the trained models to analyze URLs and generate phishing-risk predictions. 

---

# 🔮 Future Improvements

Several improvements can be explored in future versions of the project:

### Real-Time Detection

Develop a real-time phishing URL detection API capable of analyzing URLs instantly.

### Browser Extension

Create a browser extension that automatically evaluates URLs before or during website access.

### Explainable AI

Add explainability techniques so users can understand why a URL was classified as phishing.

### SHAP-Based Explanations

Use SHAP-based explanations for feature-level interpretation of Machine Learning predictions.

### Advanced Transformers

Investigate character-level Transformer architectures specifically optimized for URL sequences.

### Hybrid CNN + Transformer

Develop improved hybrid architectures combining CNN-based local feature extraction with Transformer-based contextual representation.

### Hyperparameter Optimization

Use automated hyperparameter optimization to improve model performance.

### Cross-Domain Validation

Evaluate models on URLs collected from different domains and time periods.

### Adversarial Testing

Test model robustness against deliberately modified phishing URLs.

### Zero-Day Detection

Investigate the capability of models to identify previously unseen phishing patterns.

### Online Learning

Develop mechanisms for updating the model as new phishing URLs emerge.

### Lightweight Deployment

Optimize models for browser, mobile, or edge-device deployment.

### REST API

Deploy the trained model using a FastAPI-based REST API.

### Streamlit Interface

Develop an interactive interface where users can enter URLs and receive predictions.

### Real-Time PhishTank Integration

Integrate continuously updated phishing information.

### Hybrid Reputation + ML System

Combine URL reputation information with Machine Learning predictions.

### Confidence Score

Provide a probability/confidence score with every classification.

These improvements are aligned with the project's proposed future development directions. 

---

# 🧪 Experimental Limitations

The experiments in this project use different datasets, preprocessing pipelines, feature representations, model architectures, and experimental configurations.

Therefore, results from different notebooks should **not automatically be treated as a single controlled benchmark**.

For a scientifically controlled comparison, all models would ideally use:

* The same dataset
* The same train-test split
* The same preprocessing
* The same feature representation
* The same evaluation protocol
* Consistent hyperparameter tuning methodology

The reported results should therefore be interpreted as a **collection of experimental findings across different configurations**, rather than as one perfectly controlled leaderboard. 

---

# 🔐 Security Disclaimer

This project is developed for:

* Educational purposes
* Academic research
* Defensive cybersecurity
* Machine Learning experimentation

The system is intended to assist in identifying potentially malicious URLs.

It should **not** be considered a complete replacement for:

* Enterprise security systems
* Threat intelligence platforms
* Security analysts
* Browser security mechanisms
* Human security investigation

A Machine Learning prediction should be treated as an **indicator of potential risk**, rather than absolute proof that a website is malicious or legitimate. 

---

# 🏁 Conclusion

This project demonstrates the application of **Machine Learning, Deep Learning, Natural Language Processing, and Transformer architectures** to automated phishing website detection using URL-based information.

The experiments show that different AI architectures have different strengths.

### 🏆 Traditional Machine Learning

**Random Forest** demonstrated excellent performance among the reported traditional ML models:

> **95.55% Accuracy | 95.56% Precision | 95.26% Recall | 95.41% F1-Score**

### 🤗 Transformer-Based NLP

**RoBERTa** achieved the strongest overall Transformer performance:

> **96.20% Accuracy | 96.681% Precision | 95.492% Recall | 96.083% F1-Score**

### ⚡ Computational Efficiency

**TinyBERT** achieved the fastest reported Transformer training time:

> **62.85 seconds**

### 🧠 Deep Learning

The separate comprehensive benchmark demonstrated particularly strong performance from sequence-based architectures:

> **1D CNN — 96.76% Testing Accuracy**

> **BiLSTM + Attention — 97.45% F1-Score**

> **GRU — 99.09% Recall**

Overall, the project demonstrates that phishing URL detection can benefit from multiple AI paradigms.

Traditional Machine Learning provides strong performance using structured URL characteristics, while Deep Learning and Transformer architectures provide powerful mechanisms for learning sequential and contextual URL patterns.

The experiments also demonstrate an important principle:

> **The most complex model is not necessarily the best model for every application.**

The final model should be selected by balancing:

**Accuracy + Precision + Recall + F1-Score + Computational Cost + Deployment Requirements**

The project therefore provides a comprehensive experimental foundation for developing future **real-time, adaptive, and scalable AI-based phishing detection systems**. 

---

# 👩‍💻 Author

## **Mansi Kushwaha**

**B.Tech — Electronics & Communication Engineering with Artificial Intelligence**

**Indira Gandhi Delhi Technical University for Women (IGDTUW)**

### Areas of Interest

* Artificial Intelligence
* Machine Learning
* Deep Learning
* Natural Language Processing
* Cybersecurity
* Data Science
* Generative AI

---

# ⭐ If You Find This Project Useful

If you find this project useful or interesting, consider giving the repository a ⭐ **Star**.

You can also explore the notebooks to reproduce the experiments and compare different AI approaches for phishing URL detection.

---

# 🔗 Project

**Automated Detection of Phishing Websites Through URL-Based Natural Language Processing**

The repository contains the experimental notebooks, datasets, model implementations, evaluation results, and comparative analysis used to investigate AI-based phishing URL detection. 
