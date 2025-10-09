# 📰 Fake News Detection using Machine Learning + FastAPI

This project predicts whether a news article is **Real** or **Fake** using **Natural Language Processing (NLP)** and **Machine Learning**.  
It includes **data preprocessing, model training, evaluation, and deployment** with a **FastAPI** REST API.  

---

## 🚀 Features  

- ✅ Text preprocessing (lowercasing, stopwords removal, lemmatization, HTML & link removal)  
- ✅ Different vectorization techniques tested:  
  - **CountVectorizer + Logistic Regression** → **Accuracy: 98.6%** 🎯  
  - **TF-IDF + Logistic Regression** → **Accuracy: 96.4%**  
  - **Word2Vec + Logistic Regression** → **Accuracy: 72.8%**  
- ✅ Final deployed model: **CountVectorizer + Logistic Regression**  
- ✅ FastAPI for real-time predictions (`/predict` endpoint)  
- ✅ REST API accepts raw text and returns prediction as **Real News** or **Fake News**  

---

## 📊 Dataset  

The dataset consists of **real news** and **fake news** articles.  

- `data/real` → Real news articles → labeled as **1**  
- `data/Fack` → Fake news articles → labeled as **0**  

---

## 🧹 Preprocessing Steps  

1. Lowercasing text  
2. Removing special characters  
3. Removing HTML tags & links  
4. Removing stopwords  
5. Lemmatization (WordNet)  
6. Removing extra spaces  

---

## 🧠 Models Used  

| Model | Accuracy | Notes |
|-------|----------|-------|
| CountVectorizer + Logistic Regression | **98.6%** ✅ | Final model used |
| TF-IDF + Logistic Regression | 96.4% | High accuracy but slightly lower |
| Word2Vec + Logistic Regression | 72.8% | Underperformed |

---

## INPUT
{
  "text": "Donald Trump sends out embarrassing New Year’s message."
}

## OUTPUT
"This News is Fake ⚠️☠️🚨"

OR

"This News is Real 😉"


🚀 **Live Demo**  
👉 [Try the App Here](https://news-qzod.onrender.com/docs)  


---

## ⚙️ Deployment Notes

- The API automatically downloads the NLTK `stopwords` corpus at startup if it isn't already available. Ensure the runtime has outbound internet access on first boot, or pre-package the corpus under `nltk_data/corpora/stopwords` to keep deployments fully offline.



