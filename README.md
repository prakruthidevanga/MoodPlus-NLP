# 😊 MoodPlus-NLP

**MoodPlus-NLP** is a Natural Language Processing (NLP) project that analyzes text and identifies whether the expressed sentiment is **Positive or Negative**.

The project demonstrates a complete NLP pipeline, starting from text preprocessing and feature extraction to machine learning model training, evaluation, and sentiment prediction.

---

## 📌 Project Overview

People express emotions through text in social media posts, messages, reviews, and online conversations.

MoodPlus-NLP uses **Natural Language Processing and Machine Learning** to analyze textual content and classify its sentiment.

The project uses a tweet dataset containing **40,000 tweets** and maps selected emotion categories into two main sentiment classes:

* 😊 **Positive**
* 😟 **Negative**

The NLP pipeline includes text cleaning, tokenization, stopword removal, stemming, lemmatization, text normalization, feature extraction, classification, and evaluation.

---

## 🎯 Objectives

* Understand the fundamentals of Natural Language Processing
* Clean and preprocess raw text data
* Convert text into numerical features
* Build a Machine Learning classification model
* Detect positive and negative sentiment
* Evaluate model performance using multiple metrics
* Create a simple web interface for the project

---

## 🔄 Project Workflow

```text
Raw Tweets
    ↓
Data Collection
    ↓
Text Cleaning
    ↓
Tokenization
    ↓
Stopword Removal
    ↓
Stemming & Lemmatization
    ↓
Text Normalization
    ↓
Feature Extraction
    ↓
TF-IDF / Bag of Words
    ↓
Logistic Regression
    ↓
Sentiment Prediction
    ↓
Positive / Negative
```

---

## 🧹 NLP Preprocessing

The project applies several preprocessing techniques to transform raw tweets into cleaner text.

### 1. Lowercasing

Converts all text into lowercase.

### 2. URL Removal

Removes links and URLs from tweets.

### 3. Mention Removal

Removes usernames such as `@username`.

### 4. Hashtag Removal

Removes hashtag symbols and hashtag text.

### 5. Special Character Removal

Removes unnecessary symbols and punctuation.

### 6. Number Removal

Removes numerical values from the text.

### 7. Tokenization

Breaks the sentence into individual words or tokens.

### 8. Stopword Removal

Removes commonly used words that provide limited classification information.

### 9. Lemmatization

Converts words into their meaningful base form where applicable.

### 10. Stemming

Reduces words to their root/stem form.

### 11. Repeated Character Normalization

Reduces excessive repeated characters in informal text.

The implemented preprocessing function performs these operations using **NLTK** and Python regular expressions.

---

## 📊 Dataset

The project uses a tweet emotion dataset containing **40,000 tweets**.

The original dataset contains multiple emotion categories such as:

* Happiness
* Love
* Fun
* Enthusiasm
* Relief
* Sadness
* Worry
* Hate
* Anger
* Boredom
* Neutral
* Surprise
* Empty

For this project, selected categories are mapped into two classes:

```text
Positive:
Happiness, Love, Fun, Enthusiasm, Relief

Negative:
Sadness, Worry, Hate, Anger, Boredom
```

After filtering and mapping, the notebook reports **28,348 tweets** used for the binary sentiment classification task.

---

## 🧠 Feature Extraction

Two main text representation approaches are explored.

### Bag of Words

The project uses `CountVectorizer` to represent text based on word and word-pair frequencies.

```text
Text → Words/N-grams → Numerical Features
```

### TF-IDF

TF-IDF is used to identify words that are important within the text while reducing the importance of very common terms.

The project combines:

* Word-level TF-IDF
* Character-level TF-IDF

This produces a richer representation of the tweet text.

---

## 🤖 Machine Learning Model

### Logistic Regression

The main classification model is **Logistic Regression**.

The model is trained using the combined TF-IDF features and predicts whether a tweet belongs to the positive or negative sentiment class.

Configuration used in the notebook:

```text
Model       : Logistic Regression
C           : 5
Solver      : saga
Max Iterations : 1000
```

---

## 📈 Model Performance

The current notebook reports the following evaluation results on its test set:

| Metric    |     Result |
| --------- | ---------: |
| Accuracy  | **74.16%** |
| Precision | **72.32%** |
| Recall    | **71.52%** |
| F1-Score  | **71.92%** |
| ROC-AUC   | **82.25%** |

These values are the results recorded in the repository notebook and should be understood as performance on that particular train/test split, not as a guarantee of performance on new real-world text.

---

## 🔮 Sentiment Prediction

The project includes a prediction function that accepts new text, applies the same preprocessing and feature extraction pipeline, and returns:

* Predicted sentiment
* Prediction confidence

Example:

```text
Input:
"I am so happy today, feeling absolutely great!"

Output:
Positive
```

The notebook also tests several example sentences containing positive and negative expressions.

---

## 🌐 Web Interface

The repository also contains an HTML prototype:

```text
Moodpulse_Website_NLP.html
```

This provides a simple web-based interface for presenting the MoodPlus NLP concept. The repository currently includes the HTML prototype along with the NLP notebook and project report.

---

## 🛠️ Technology Stack

### Programming Language

* Python

### NLP

* NLTK
* Tokenization
* Stopword Removal
* Stemming
* Lemmatization
* Text Normalization

### Machine Learning

* Scikit-learn
* Logistic Regression
* Train-Test Split
* Classification Metrics

### Data Processing

* Pandas
* NumPy
* SciPy

### Visualization

* Matplotlib
* Seaborn

### Web

* HTML
* CSS
* JavaScript

---

---

## 🚀 How to Run the NLP Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/prakruthidevanga/MoodPlus-NLP.git
```

### Step 2: Open the Notebook

Open:

```text
Emotion_Detection_NLP_Code.ipynb
```

using **Google Colab** or **Jupyter Notebook**.

### Step 3: Add the Dataset

Make sure the required:

```text
tweet_emotions.csv
```

dataset is available in the notebook environment.

### Step 4: Install Required Libraries

```bash
pip install numpy pandas scipy matplotlib seaborn nltk scikit-learn
```

### Step 5: Run the Notebook

Run the notebook cells from top to bottom.

The notebook downloads the required NLTK resources and performs the complete NLP pipeline.

---

## 🌟 Key Learning Outcomes

Through this project, I explored:

* Natural Language Processing
* Text preprocessing
* Tokenization
* Stopword removal
* Stemming
* Lemmatization
* Bag of Words
* TF-IDF
* Machine Learning classification
* Logistic Regression
* Model evaluation
* Sentiment prediction
* NLP data visualization
* Basic web integration

---

## 🔮 Future Enhancements

Possible improvements include:

* Support for multiple emotion classes instead of only positive/negative
* Use of advanced NLP models such as BERT
* Real-time sentiment analysis
* Improved handling of sarcasm and slang
* Multilingual sentiment analysis
* Interactive dashboard
* REST API for predictions
* Deployment as a web application
* Real-time social media text analysis

---

## 👩‍💻 Author

### Prakruthi BR

BCA – Artificial Intelligence & Machine Learning


---

## ⭐ Project

If you find this project useful or interesting, consider giving the repository a ⭐.

**Repository:**
https://github.com/prakruthidevanga/MoodPlus-NLP
