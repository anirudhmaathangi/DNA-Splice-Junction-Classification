DNA Splice Junction Classification using Machine Learning

## Project Overview

This project builds a machine learning model to classify DNA splice junction sequences into three categories:

1. EI — Exon-Intron boundary
2. IE — Intron-Exon boundary
3. N — Neither

The goal is to predict splice junction type from a 60-base DNA sequence using supervised learning.



## Dataset

Dataset used: UCI Molecular Biology (Splice Junction Gene Sequences)

* ~3190 DNA sequences
* Each sequence length: 60 nucleotides
* Classes: EI, IE, N
* Features: nucleotide at each position (A, C, G, T, N)

Rare ambiguity characters (D, S, R) were replaced with N during preprocessing.



## Data Preprocessing

Steps performed:

* Removed sequence ID column
* Cleaned rare nucleotide symbols
* Converted sequences into positional features
* One-hot encoded nucleotides
* Train-test split (80-20)



## Models Used

The following models were trained and compared:

* Random Forest Classifier
* Logistic Regression
* Support Vector Machine (SVM)
* XGBoost Classifier



## Results

| Model               | Accuracy |
| ------------------- | -------- |
| Random Forest       | ~93%     |
| Logistic Regression | ~95%     |
| SVM                 | ~96%     |
| XGBoost             | ~97%     |

XGBoost achieved the best performance.



## Evaluation Metrics

Models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix



## Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Matplotlib



## How to Run

1. Open the notebook in Google Colab
2. Upload `splice.data` dataset
3. Run cells sequentially
4. Models will train and display evaluation metrics



## Author

Maathangi Anirudh
