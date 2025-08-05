Real-Time Toxic Comment Detection System

Problem Statement:

The goal is to develop a real-time system that can detect toxic and offensive comments in online platforms. The system should classify comments based on six types of toxicity:

Toxic

Severe Toxic

Obscene

Threat

Insult

Identity Hate

Tools and Technologies Used:

Programming Language: Python

Libraries: sklearn, nltk, joblib, gradio, pandas, numpy

ML Model: Logistic Regression with OneVsRestClassifier

Feature Engineering: TF-IDF Vectorization

Interface: Gradio Web UI

Dataset: Jigsaw Toxic Comment Classification Dataset (Kaggle)

Project Features:

Multi-label classification for toxic comment types.

Real-time prediction through a Gradio web interface.

Keyword highlighting of toxic terms in the user input.

Evaluation using metrics like Hamming Loss, Jaccard Score, ROC AUC, and Subset Accuracy.

Model and vectorizer are saved and reused for deployment.

Methodology:

1.Data Acquisition : Used train.csv from the Jigsaw dataset with 6 binary toxicity labels.

2.Text Preprocessing : Lowercasing, punctuation & digit removal, stop word removal, lemmatization (using NLTK).

3.Feature Extraction : TF-IDF (unigrams and bigrams), with max 15,000 features.

4.Model Training : 

    -Logistic Regression inside a OneVsRestClassifier for multi-label learning.

    -class_weight='balanced' for label imbalance handling.

5.Model Evaluation : Hamming Loss, Jaccard Score, Subset Accuracy, ROC AUC, and per-label Precision/Recall.

6.Web Interface : Built using Gradio with real-time text analysis and keyword highlighting.

Results Snapshot:

Subset Accuracy: 88.40%

Hamming Loss: 2.96%

Jaccard Score: 4.87%

Best ROC AUC: ~97.3% (for obscene, threat, severe_toxic)

