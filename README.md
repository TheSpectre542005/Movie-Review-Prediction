# 🎬 Movie Review Sentiment Analysis – Practical 8

## Student Information
- **Name:** Rishil Pawar
- **Roll No.:** C1-18
- **Subject:** NLP Lab (Practical 8)

## Project Overview
A complete **Movie Review Sentiment Analysis** system built using Natural Language Processing (NLP) techniques. The project classifies IMDB movie reviews as **Positive** or **Negative** using machine learning models, with a GUI-based prediction interface.

## Dataset
- **GitHub:** [Movie-Review-Prediction](https://github.com/TheSpectre542005/Movie-Review-Prediction)
- **Source:** [IMDB Dataset (Kaggle)](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)
- **Size:** 50,000 movie reviews (25,000 positive + 25,000 negative)
- **Columns:** `review` (text), `sentiment` (positive/negative)

## Implementation Steps

### 1. Install & Import Libraries
- pandas, numpy, nltk, scikit-learn, matplotlib, seaborn, gradio, pickle

### 2. Load & Explore Dataset (EDA)
- Dataset shape: `(50000, 2)`
- Balanced classes: 25,000 each
- Visualizations: Bar chart & Pie chart for class distribution

### 3. Text Preprocessing
- Lowercasing, HTML tag removal, special character removal
- Stopword removal (NLTK English stopwords)
- Porter Stemming
- Label encoding: positive → 1, negative → 0

### 4. Feature Extraction (TF-IDF)
- TF-IDF Vectorizer with `max_features=10000`, `ngram_range=(1,2)`, `min_df=2`
- Train-test split: 80-20 (stratified)

### 5. Model Training & Evaluation
Five models trained and compared:

| Model | Accuracy % | Precision % | Recall % | F1-Score % | Time (s) |
|---|---|---|---|---|---|
| **Logistic Regression** | **89.05** | **88.43** | **89.86** | **89.14** | 1.27 |
| Linear SVM | 88.77 | 88.17 | 89.56 | 88.86 | 3.36 |
| Multinomial Naive Bayes | 86.35 | 85.00 | 88.28 | 86.61 | 0.08 |
| Random Forest | 85.00 | 85.21 | 84.70 | 84.95 | 126.87 |
| Gradient Boosting | 81.27 | 78.25 | 86.62 | 82.22 | 164.44 |

### 6. Best Model Selection
- **Selected Model:** Logistic Regression
- **Accuracy:** 89.05%
- **F1-Score:** 89.14%

### 7. Model Saving
- Best model saved as `best_model.pkl`
- TF-IDF vectorizer saved as `tfidf_vectorizer.pkl`

### 8. GUI-based Prediction (Gradio)
- Interactive web interface for real-time sentiment prediction
- Accepts movie review text input
- Returns sentiment label (Positive/Negative) with confidence score
- Built using **Gradio** framework

## How to Run
1. Open the notebook in Google Colab
2. Run all cells sequentially
3. The Gradio interface will launch automatically with a shareable link

## Project Structure
```
Movie-Review-Sentiment-Analysis/
├── Practical_8_Sentiment_Analysis (1).ipynb    # Complete Colab notebook
├── Practical_8_Movie_Review_Sentiment_Analysis_Report.docx  # Word document report
├── README.md                                    # This file
└── create_report.py                             # Script to generate the report
```

## Technologies Used
- Python 3.x
- pandas, numpy, nltk, scikit-learn
- matplotlib, seaborn
- Gradio
- Google Colab

## License
This project is for educational purposes only.
