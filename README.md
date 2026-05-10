# 📰 Fake News Headline Detector

**Digital Skills for Students Program | Enhancing Digital Government & Economy (EDGE) Project** **Course:** Applied Machine Learning (Project 11)  
**Domain:** NLP / Media Literacy  

## 📌 Project Overview
[cite_start]The proliferation of fake news poses serious risks to public discourse and democratic processes[cite: 10]. [cite_start]This project builds a binary text classifier that distinguishes real from fabricated news headlines, featuring an explainability layer that highlights the suspicious words or phrases that influenced the model's decision[cite: 11]. 

[cite_start]The included graphical user interface (GUI) simulates a browser extension that a journalist or reader might use to fact-check a headline before sharing[cite: 12].

## 📊 Dataset
[cite_start]This project uses the **Fake and Real News Dataset** from Kaggle[cite: 32]. 
* [cite_start]**Labels:** REAL (0) / FAKE (1) [cite: 36]
* [cite_start]**Features:** TF-IDF extraction (Unigrams + Bigrams, capped at 10,000 features)[cite: 37].

## ⚙️ Machine Learning Pipeline
The project was developed in 5 distinct phases:

1. [cite_start]**Data Loading & EDA:** Analyzed class distribution, average headline lengths, and generated word clouds for both REAL and FAKE classes[cite: 41]. [cite_start]Extracted the top 20 most discriminative TF-IDF terms[cite: 42].
2. [cite_start]**Text Preprocessing:** Lowercased text, removed punctuation, stripped English stop-words, and lemmatized the text using the NLTK `WordNetLemmatizer`[cite: 44].
3. [cite_start]**Model Training:** Trained three models using 5-fold stratified cross-validation[cite: 46]:
   * **Logistic Regression:** Used as the baseline model.
   * **Multinomial Naive Bayes:** A probabilistic baseline.
   * [cite_start]**LSTM (Long Short-Term Memory):** A deep learning neural network utilizing an Embedding layer and Keras tokenization[cite: 46].
4. [cite_start]**Evaluation:** Evaluated models using Accuracy, Precision, Recall, F1-Score, and AUC-ROC curves[cite: 47]. [cite_start]Generated confusion matrices and plotted the top 20 features most predictive of fabricated news[cite: 47].
5. [cite_start]**Interactive GUI:** Built a live Gradio web application that accepts user input, displays a verdict with a confidence score, and highlights suspicious words in red[cite: 48, 49].

## 🚀 How to Run the Project
1. Clone this repository: `git clone https://github.com/yourusername/fake-news-detector.git`
2. Install the required dependencies: `pip install -r requirements.txt`
3. Download the Kaggle Fake and Real News Dataset and place `True.csv` and `Fake.csv` in the project root directory.
4. Run the Jupyter Notebook (`Fake_News_Detector.ipynb`) to see the EDA, model training, and launch the Gradio interface.

## ⚠️ Limitations & Disclaimer
[cite_start]**No automated tool can replace fact-checking by a trained journalist**[cite: 70]. This system detects linguistic patterns and sensationalist structures common in fabricated headlines, but it does not verify factual accuracy.

---
*Instructors: Prof. Dr. Fazlul Hasan Siddiqui & Md. Rahad Khan | [cite_start]DUET, Gazipur* [cite: 77]
