# Project 3: Medical Text Classification  

This repository contains the implementation of a **medical transcript classification system** using Natural Language Processing (NLP) techniques. The project explores both **Binary Bag-of-Words (BBoW)** and **Frequency Bag-of-Words (FBoW)** text vectorization methods combined with multiple machine learning classifiers.  

## 📌 Project Overview  

The task is to classify **medical transcripts** into one of four categories:  
1. **Surgery**  
2. **Medical Records**  
3. **Internal Medicine**  
4. **Other**  

The dataset is split as follows:  
- **Training:** 4000 transcripts  
- **Validation:** 500 transcripts  
- **Testing:** 500 transcripts  

## 🔑 Key Steps  

### 1. **Text Vectorization**  
Since machine learning models require fixed-length vectors, transcripts are represented in two ways:  

- **Binary Bag-of-Words (BBoW):**  
  - Build vocabulary from training data only.  
  - Preprocess by lowercasing and removing punctuation.  
  - Keep top 10,000 frequent words.  
  - Encode presence/absence of words (1 or 0).  

- **Frequency Bag-of-Words (FBoW):**  
  - Same preprocessing and vocabulary construction.  
  - Represent each word by normalized frequency so vectors sum to 1.  

### 2. **Classification with BBoW**  
Models trained and evaluated using the **F1-score**:  
- Logistic Regression  
- Decision Tree  
- Random Forest  
- XGBoost  

Metrics are reported for **training, validation, and test sets**.  

### 3. **Classification with FBoW**  
- Same classifiers trained with **frequency-based representation**.  
- Comparison between BBoW and FBoW to determine which performs better and why.  

## 📂 Deliverables  

- **Vocabulary file**: word → ID → frequency  

      the 1 20456


- **Dataset format (Train/Valid/Test):** word IDs per line with class label at the end  

      100 8 3 1034 0


## 🛠️ Technologies Used  

- Python 3  
- Pandas / NumPy (data handling)  
- Scikit-learn (Logistic Regression, Decision Tree, Random Forest)  
- XGBoost (classification)  
- NLTK / re (text preprocessing)  

## 🚀 How to Run  

Clone the repository:
   
       git clone https://github.com/your-username/project3-medical-text-classification.git
       cd project3-medical-text-classification

Install dependencies:

    pip install numpy pandas scikit-learn xgboost nltk

Preprocess data & train models (example script):

    python main.py --mode train --vectorizer bbow

Evaluate on validation/test sets:

    python main.py --mode eval --vectorizer fbow

## 📊 Expected Outputs
- F1-scores for training, validation, and test sets.
- Comparison of models and vectorization methods.
- Analysis of hyperparameters (e.g., depth of trees, learning rate in XGBoost).
