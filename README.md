Homeassignment4
README - Home Assignment 4 (Neural Networks and Deep Learning)
Student Information
Name: Jaswanth Reddy Donapati Course: CS5720 Neural Networks and Deep Learning
University: University of Central Missouri
Student ID : 700757646 

Description
This repo contains solutions for the following NLP and Attention-related tasks:

NLP Preprocessing (Tokenization, Stopword Removal, Stemming)
Named Entity Recognition using SpaCy
Scaled Dot-Product Attention implementation from scratch
Sentiment Analysis using HuggingFace Transformers
Run Instructions
All scripts are written in Python 3
Install dependencies using:
pip install nltk spacy transformers
python -m nltk.downloader punkt stopwords
python -m spacy download en_core_web_sm


Q1: NLP Preprocessing
1. Difference between Stemming and Lemmatization

Stemming cuts off word suffixes based on simple rules.

Ex: "running" → "run"

Lemmatization returns the base dictionary form of a word, using linguistic knowledge.

Ex: "running" → "run" (but "better" → "good")

Lemmatization is more accurate but slower. Stemming is faster but may not return valid words.

2. Why Remove Stop Words?

Useful:

Speeds up processing

Reduces noise in classification tasks (like spam detection or sentiment analysis)

Harmful:

Can remove meaningful context in some cases (e.g., "to be or not to be" — all are stop words!)


Q2: Named Entity Recognition (NER)
1. NER vs POS Tagging


NER	POS Tagging
Finds named entities (e.g., persons, orgs, dates)	Tags parts of speech (noun, verb, etc.)
Focuses on real-world objects	Focuses on grammar structure
2. Real-World Applications of NER

Finance: Automatically identify companies, currencies, and dates in stock market news.

Search Engines: Highlight entities in queries like “CEO of Tesla in 2022”.

Q3: Scaled Dot-Product Attention
1. Why Divide by √d?

To prevent large dot-product values from causing the softmax to saturate, which would result in tiny gradients and hurt learning. Dividing by √d (where d = key size) keeps values well-scaled.

2. How Self-Attention Helps

Self-attention lets each word attend to all other words in the sentence — so the model can learn:

Context (e.g., "bank" in “river bank” vs “money bank”)

Word dependencies regardless of position

Q4: HuggingFace Sentiment Analysis
1. Difference Between BERT and GPT


Model	Architecture	Used For
BERT	Encoder-only	Good for classification, question answering
GPT	Decoder-only	Good for text generation, chatbots
2. Why Use Pretrained Models?

Saves time and compute

Trained on massive datasets (e.g., Wikipedia, Books)

Achieve high performance even with small fine-tuning datasets
