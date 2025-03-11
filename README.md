# Detecting-Amazon-SPAM-Reviews-using-Text-Mining-and-NLP

Team Members:
Divyam Rana,
Donghyeon Na,
Pushpraj Singh,
Aaryan Bammi,

**Project Overview**:
Fake or spam reviews on e-commerce platforms, such as Amazon, impact customer trust and purchase decisions. This project aims to develop a machine learning model to classify Amazon product reviews as spam (1) or non-spam (0), improving credibility and user experience.

**Dataset Overview**:
The dataset consists of 5.5 million Amazon product reviews from the Clothing, Shoes, and Jewelry category. The dataset was processed and downsampled to 450K balanced reviews (50-50 spam/non-spam). 

**The key features include:**

Target Variable: class (1: spam / 0: non-spam)

Numerical Features: helpful (helpful votes & total votes),overall (review rating score),unixReviewTime (timestamp)

Categorical Features:reviewerID, asin, reviewerName, category

Text Features:reviewText, summary, 

**Data Preprocessing & Feature Engineering**

**The data pipeline includes:**

**Text Cleanup**: Removing stopwords, special characters, and lemmatization.

**Feature Engineering:**

TF-IDF vectorization
Word Embeddings (Word2Vec, MiniLM-L6-v2)
Cosine Similarity: Measures similarity between reviews.

**Additional Textual Features:**

Review length
Number of unique words
Flesch readability score
Vader sentiment score
Part-of-Speech (POS) counts (nouns, adverbs, adjectives, etc.)

**Data Standardization:**

Normalization of numerical features.
Class Balancing: Downsampled spam and non-spam reviews to 50-50.

**Model Selection & Training**

The project tested various machine learning models:

Logistic Regression (SGD)

Support Vector Machine (SVM)

Random Forest

Voting Classifier (Ensemble approach)

Best Model: Voting Classifier
Accuracy: 84%
Precision/Recall: Balanced across spam and non-spam classes.

**Key Results**

Model	Precision	Recall	Accuracy

Logistic Regression (SGD)	0.82	0.81	82%

Support Vector Machine (SVM)	0.83	0.81	82%

Random Forest	0.84	0.83	84%

Voting Classifier (Best Model)	0.84	0.84	84%

**Future Enhancements**

Neural Networks: Experimenting with transformer-based models (BERT, RoBERTa).

Real-Time Processing: Deploying the pipeline for streaming data detection.

Additional Features: Improving feature extraction with topic modeling or more complex embeddings.
