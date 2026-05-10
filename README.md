# 📰 Fake News Headline Detector

**Digital Skills for Students Program | Enhancing Digital Government & Economy (EDGE) Project** **Course:** Applied Machine Learning (Project 11)  
**Domain:** NLP / Media Literacy  

## 📌 Project Overview
The proliferation of fake news poses serious risks to public discourse and democratic processes. This project builds a binary text classifier that distinguishes real from fabricated news headlines, featuring an explainability layer that highlights the suspicious words or phrases that influenced the model's decision. 

The included graphical user interface (GUI) simulates a browser extension that a journalist or reader might use to fact-check a headline before sharing.

## 📊 Dataset
This project uses the **Fake and Real News Dataset** from Kaggle. 
* **Labels:** REAL (0) / FAKE (1)
* **Features:** TF-IDF extraction (Unigrams + Bigrams, capped at 10,000 features).

## ⚙️ Machine Learning Pipeline
The project was developed in 5 distinct phases:

1. **Data Loading & EDA:** Analyzed class distribution, average headline lengths, and generated word clouds for both REAL and FAKE classes. Extracted the top 20 most discriminative TF-IDF terms.
2. **Text Preprocessing:** Lowercased text, removed punctuation, stripped English stop-words, and lemmatized the text using the NLTK `WordNetLemmatizer`.
3. **Model Training:** Trained three models using 5-fold stratified cross-validation:
   * **Logistic Regression:** Used as the baseline model.
   * **Multinomial Naive Bayes:** A probabilistic baseline.
   * **LSTM (Long Short-Term Memory):** A deep learning neural network utilizing an Embedding layer and Keras tokenization.
4. **Evaluation:** Evaluated models using Accuracy, Precision, Recall, F1-Score, and AUC-ROC curves. Generated confusion matrices and plotted the top 20 features most predictive of fabricated news.
5. **Interactive GUI:** Built a live Gradio web application that accepts user input, displays a verdict with a confidence score, and highlights suspicious words in red.

## 🚀 How to Run the Project
1. Clone this repository: `git clone https://github.com/yourusername/fake-news-detector.git`
2. Install the required dependencies: `pip install -r requirements.txt`
3. Download the Kaggle Fake and Real News Dataset and place `True.csv` and `Fake.csv` in the project root directory.
4. Run the Jupyter Notebook (`Fake_News_Detector.ipynb`) to see the EDA, model training, and launch the Gradio interface.

## ⚠️ Limitations & Disclaimer
**No automated tool can replace fact-checking by a trained journalist**. This system detects linguistic patterns and sensationalist structures common in fabricated headlines, but it does not verify factual accuracy.

---
*Instructors: Prof. Dr. Fazlul Hasan Siddiqui & Md. Rahad Khan | DUET, Gazipur*
