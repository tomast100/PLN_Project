# Natural Language Processing Projects

![Python](https://img.shields.io/badge/Python-NLP-blue)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange)
![Machine Learning](https://img.shields.io/badge/Approach-ML%20%2B%20Transformers-green)
![Dataset](https://img.shields.io/badge/Dataset-FactNews-lightgrey)

This repository contains two projects developed for the **Natural Language Processing** course at **FEUP**, both focused on sentence-level classification using the FactNews dataset.

The repository is organized as a small project portfolio around the same academic context:
- **Assignment 1** explores traditional NLP and machine learning pipelines.
- **Assignment 2** explores Transformer-based approaches with Hugging Face.

---

## Overview

The two notebooks study the same general problem from different perspectives.

- **Project 1** builds strong classical baselines using preprocessing, feature engineering, and traditional classifiers.
- **Project 2** moves to modern Transformer models to evaluate whether contextual language representations improve performance on the same tasks.

Together, they provide a clear progression from **interpretable traditional NLP methods** to **state-of-the-art deep learning approaches** for Portuguese text classification.

---

## Repository Structure

```bash
.
├── assignment_1.ipynb
└── assignment_2.ipynb
```

| File | Description |
|------|-------------|
| `assignment_1.ipynb` | Traditional NLP and machine learning classifiers for FactNews |
| `assignment_2.ipynb` | Transformer-based experiments using Hugging Face models |

---

## Dataset

Both projects use the **FactNews** dataset, a Brazilian Portuguese sentence-level dataset designed for factuality and media-bias analysis.

The notebooks work with two task formulations:
- **Task A** — 3-class classification: `biased`, `factual`, `quote`
- **Task B** — binary classification: `factual`, `nonfactual`

The dataset includes:
- **6,191 annotated sentences**
- **300 news documents**
- **100 news stories**
- Content from **Folha de São Paulo, Estado, and O Globo**
- Multiple domains such as politics, world, sports, daily news, culture, and science

---

## Project Summary

| Project | Main Focus | Core Methods | Goal |
|--------|------------|--------------|------|
| **Assignment 1** | Traditional NLP pipelines | TF-IDF, Bag-of-Words, Word2Vec, Logistic Regression, Naive Bayes, LinearSVC | Build strong non-neural baselines and analyze their behavior |
| **Assignment 2** | Transformer-based classification | Hugging Face, fine-tuning, mBERT, Albertina, imbalance handling | Evaluate whether Transformer models improve sentence classification performance |

---

## Assignment 1

### Traditional NLP Classifiers for FactNews

This notebook focuses on a full traditional machine learning workflow for sentence classification.

Main components:
- Exploratory data analysis over labels and corpus characteristics
- Text preprocessing and normalization
- Sparse and dense text representations
- Baseline and supervised classifiers
- Evaluation with class-aware metrics
- Error analysis and discussion of class imbalance

### Techniques used

- **Preprocessing:** lowercasing, URL removal, digit removal, punctuation cleanup, whitespace normalization
- **Representations:** Bag-of-Words, TF-IDF, mean Word2Vec embeddings
- **Models:** DummyClassifier, Logistic Regression, Multinomial Naive Bayes, Complement Naive Bayes, LinearSVC
- **Imbalance handling:** experiments with resampling methods such as SMOTE and BorderlineSMOTE

### Why this project matters

This notebook shows that carefully designed traditional NLP pipelines can remain very competitive, especially when lexical cues are strong and interpretability matters.

---

## Assignment 2

### Transformer Models for FactNews

This notebook extends the same problem setting with Transformer-based models using the Hugging Face ecosystem.

Main components:
- Dataset preparation for Transformer training
- Tokenization and sequence classification setup
- Fine-tuning experiments with pretrained language models
- Evaluation across the same task formulations
- Experiments for dealing with class imbalance

### Techniques used

- **Frameworks:** PyTorch, Hugging Face Transformers, Datasets, Accelerate
- **Models explored:** multilingual and Portuguese-oriented Transformer models, including **mBERT** and **Albertina**
- **Strategies:** fine-tuning, class-weighted loss, manual oversampling, model comparison

### Why this project matters

This notebook complements the first assignment by testing whether contextual embeddings and pretrained Transformer models capture factuality and bias cues more effectively than classical feature-based models.

---

## Installation

A typical setup can be created with Python and Jupyter.

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd <your-repository-name>
```

### 2. Create a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate
```

### 3. Install the main dependencies

For the first notebook:

```bash
pip install pandas numpy matplotlib scikit-learn nltk gensim wordcloud imbalanced-learn
```

For the second notebook:

```bash
pip install torch torchvision torchaudio
pip install datasets transformers accelerate
```

If you want a single environment for both notebooks, you can install all of the packages above in the same virtual environment.

---

## Running the Projects

Open the notebooks with Jupyter:

```bash
jupyter notebook
```

Recommended order:
1. Start with `assignment_1.ipynb` to understand the dataset, preprocessing choices, and strong classical baselines.
2. Then open `assignment_2.ipynb` to compare those baselines with Transformer-based approaches.

> **Note:** data loading is handled differently across the notebooks, so you may need to adapt file paths depending on your local setup.

---

## Learning Outcomes

These projects demonstrate practical experience with:

- Text preprocessing and normalization
- Feature engineering for NLP
- Supervised text classification
- Evaluation under class imbalance
- Comparative analysis between traditional ML and Transformers
- Portuguese-language NLP workflows
- Experimentation in Jupyter notebooks

---

## Authors

Developed by:

- **Elton Tamele**
- **Maureen Ah-sh**
- **Toms Teixeira**

for the **Natural Language Processing** course in **MEIC, FEUP**.

