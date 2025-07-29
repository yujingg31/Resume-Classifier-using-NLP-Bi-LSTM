# Resume-Classifier-using-NLP-Bi-LSTM
An NLP-powered resume classification application that uses deep learning (Bi-LSTM) to automate the process of sorting resumes into predefined job categories. 
___

## 🚀 Project Objectives
- Collect and preprocess a corpus of resumes from various job domains.
- Apply NLP vectorization techniques (Word2Vec, GloVe, etc.) for feature extraction.
- Build a classification model using deep learning (Bi-LSTM).
- Evaluate performance using accuracy, precision, recall, and F1-score.
- Deploy a local web application prototype for resume classification.

## 📦 Dataset
- Format: PDF resumes
- Job domains: 24 (e.g., HR, Engineering, Accountant, Designer, etc.)

## Data Preprocessing Pipeline
- PDF Text Extraction using PyPDF2
- Cleaning: HTML tag removal, stopwords, punctuation, special characters
- Tokenization using nltk.punkt
- Lemmatization using nltk.wordnet
- Vocabulary Encoding & Padding
- Label Encoding for classification
- Data augmentation techniques: random word swapping, random word insertion

## Model Architecture
2 Layers of Bidirectional LSTM
Embedding Dimension: 100
Hidden Layer Size: 64
Output: Fully Connected Dense Layer for Classification
Optimizer: Adam
Loss function: Cross-Entropy
Training-Validation-Test Split: 70%-15%-15%
Early stopping & custom weight initialization

## Results
Overall Accuracy: 69%
Macro Avg F1-Score: 0.62
Weighted Avg F1-Score: 0.68
| Job Role    | Precision | Recall | F1-Score |
| ----------- | --------- | ------ | -------- |
| HR          | 1.00      | 1.00   | 1.00     |
| Accountant  | 0.94      | 1.00   | 0.97     |
| Designer    | 0.94      | 1.00   | 0.97     |
| Engineering | 0.94      | 1.00   | 0.97     |

## Future Work
- Improve performance for underrepresented classes like BPO, Agriculture
- Implement advanced transformers (e.g., BERT) for context-aware embeddings
- Expand dataset and deploy web application prototype
- Support multi-language resume parsing


