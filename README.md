DABERT-ABSA: Dependency-Aware BERT for Aspect-Based Sentiment Analysis
Overview

DABERT-ABSA is a transformer-based Aspect-Based Sentiment Analysis (ABSA) framework designed to improve fine-grained sentiment understanding in multi-aspect sentences. The model combines DistilBERT, dependency-based clause splitting, BIO tagging, and multi-head cross-attention to accurately identify aspect terms and classify their sentiments independently.

This project was developed as a research-oriented NLP system focused on reducing cross-clause sentiment interference while maintaining high performance with a lightweight transformer architecture.

Features
Aspect Term Extraction using BIO tagging
Aspect Sentiment Classification with Cross-Attention
Dependency-based clause segmentation using spaCy
Multi-dataset training pipeline
DistilBERT-powered contextual embeddings
Reduced parameter count compared to BERT-base
Strong cross-dataset generalization
Architecture

The framework consists of four major components:

DistilBERT Encoder
Generates contextual token embeddings
BIO Tagging Head
Detects aspect term spans
Dependency-Based Clause Splitting
Splits multi-aspect sentences into independent clauses
Cross-Attention Sentiment Classifier
Focuses attention on aspect-specific sentiment tokens
Datasets Used

The model was trained and evaluated on:

SemEval 2014 Restaurant
SemEval 2015 Restaurant
SemEval 2016 Restaurant
MAMS Dataset
Model Performance
Aspect Term Extraction
Model	F1 Score
BERT-base	0.7896
Proposed Model	0.7888
Sentiment Classification (REST14)
Metric	Score
Accuracy	0.8406
Macro-F1	0.8375
Key Improvements
48.9% reduction in Cross-Clause Interference Rate
Higher attention localization than BERT-base
~40% fewer parameters than BERT-base
Tech Stack
Python
PyTorch
Hugging Face Transformers
DistilBERT
spaCy
scikit-learn
seqeval
Installation
git clone https://github.com/your-username/DABERT-ABSA.git
cd DABERT-ABSA
pip install -r requirements.txt
Usage
Train the Model
python train.py
Run Inference
python inference.py
Example
Input
"The service was slow, but the staff were very friendly."
Output
(service, negative)
(staff, positive)
Research Contributions
Introduced dependency-aware clause segmentation for ABSA
Proposed Cross-Clause Interference Rate (CCIR)
Proposed Attention Focus Score (AFS)
Demonstrated efficient transformer-based ABSA with fewer parameters
Future Improvements
Cross-domain ABSA training
Emotion-aware sentiment prediction
Multilingual support
Implicit aspect detection
