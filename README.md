# 💬 Score-based Sentiment Classification : Comments from Reddit

## 📌 Project Overview

This project focuses on predicting Reddit comment engagement and sentiment using large-scale social media data. Leveraging the Kaggle 1M Reddit Comments dataset, the system classifies comments by engagement level and sentiment polarity.

To balance scalability and performance, a 30,000-comment subset was sampled from both balanced and imbalanced distributions, enabling a controlled comparison between traditional NLP baselines and transformer-based models.

## 📊 Dataset

Source: Kaggle – 1M Reddit Comments

**https://www.kaggle.com/datasets/smagnan/1-million-reddit-comments-from-40-subreddits**

Subsample used: 30,000 comments

Data splits: Balanced and imbalanced subsets

Tasks:

Engagement-level classification

Sentiment classification (Positive / Neutral / Negative)

## 🔎 Feature Extraction & Text Representation

TF-IDF Vectorization for traditional ML models

RoBERTa embeddings via fine-tuning for contextual sentiment understanding

This dual approach enables direct performance comparison between bag-of-words baselines and context-aware transformer models.

## 🤖 Models Implemented
**🔹 TF-IDF + Logistic Regression (Baseline):**

Evaluated on both balanced and imbalanced datasets to quantify the impact of class imbalance:

Balanced Dataset:

Negative: 0.41

Neutral: 0.39

Positive: 0.40

Imbalanced Dataset:

Negative: 0.11

Neutral: 0.45

Positive: 0.54

These results highlight the sensitivity of traditional models to class imbalance.

**🔹 RoBERTa (Fine-Tuned):**

RoBERTa was fine-tuned for sentiment classification, demonstrating improved performance through contextual language understanding.

F1-Scores (30k dataset):

Positive: 0.65

Neutral: 0.47

Negative: 0.11

The transformer-based approach outperformed the baseline, particularly for positive and neutral sentiment classes.

## 📈 Evaluation Metrics

F1 Score (per class)

Performance comparison across balanced vs. imbalanced data distributions

F1-score was selected due to its robustness to class imbalance and relevance in multi-class classification tasks.

## ✅ Key Insights

Transformer-based models significantly outperform TF-IDF baselines for sentiment analysis

Traditional models degrade sharply under class imbalance

Subsampling enables efficient experimentation without sacrificing meaningful insights

Contextual embeddings are critical for capturing nuanced user sentiment in social media text

## 🌍 Applications

Social media analytics

Content moderation and recommendation systems

User engagement prediction

Opinion mining at scale

## 🔮 Future Work

Full-scale training on the complete 1M-comment dataset

Advanced imbalance handling (focal loss, class weighting)

Joint modeling of engagement and sentiment

Deployment as a real-time inference API
