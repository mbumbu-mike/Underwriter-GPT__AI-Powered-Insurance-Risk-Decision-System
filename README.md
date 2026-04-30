# 🚗 Underwriter-GPT

### AI-Powered Insurance Risk Decision System

## 📌 Overview

Underwriter-GPT is an intelligent decision-support system for insurance underwriting. It combines **machine learning** and **LLM-powered explanations** to assess customer risk and provide transparent, data-driven decisions.

The system predicts whether a policy applicant is **low**, **medium**, or **high risk**, and explains the reasoning using similar historical cases.

---

## 🎯 Problem Statement

Insurance underwriting decisions are often:

* Time-consuming
* Inconsistent
* Difficult to explain

This project solves that by building a system that:

* Predicts **risk scores** using historical data
* Retrieves **similar past policies**
* Generates **human-like explanations** for decisions

---

## 🧠 System Architecture

User Input → ML Model → Risk Score
          ↓
      FAISS Retrieval (Similar Cases)
          ↓
      LLM Explanation (RAG)
          ↓
      Final Decision Output

---

## ⚙️ Core Components

### 1. Risk Prediction Model

* Supervised ML model trained on insurance data
* Target: `claim_status`
* Outputs probability of claim (risk score)

### 2. Retrieval-Augmented Generation (RAG)

* Converts past policies into text summaries
* Uses embeddings + FAISS for similarity search
* Retrieves relevant historical cases

### 3. Explanation Engine

* Uses an LLM to generate underwriter-style reasoning
* Combines:

  * Model prediction
  * Retrieved similar cases

### 4. Web Application

* User inputs policy details
* System returns:

  * Risk score
  * Decision (Accept / Review / Reject)
  * Explanation

---

## 📊 Dataset

The dataset contains vehicle insurance policy data including:

* Customer demographics (age, region)
* Vehicle attributes (age, engine, fuel type)
* Safety features (ESC, airbags, TPMS, etc.)
* Policy details
* Claim history (`claim_status`)

---

## 🚀 Features

* ✅ Risk scoring using machine learning
* ✅ Explainable AI using LLM + RAG
* ✅ Similar case retrieval (evidence-based decisions)
* ✅ Clean API for integration
* ✅ Interactive web interface

---

## 🛠️ Tech Stack

**Backend**

* Python
* FastAPI

**Machine Learning**

* Scikit-learn / XGBoost
* SHAP (for feature importance)

**RAG Pipeline**

* SentenceTransformers
* FAISS

**Frontend**

* Streamlit (initial)
* Next.js (future upgrade)

---

## 📂 Project Structure

```
underwriter-gpt/
│
├── data/
│   ├── raw/
│   ├── processed/
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_model_training.ipynb
│
├── src/
│   ├── model/
│   │   ├── train.py
│   │   ├── predict.py
│   │
│   ├── rag/
│   │   ├── embed.py
│   │   ├── retrieve.py
│   │
│   ├── api/
│   │   ├── main.py
│
├── app/
│   ├── streamlit_app.py
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## ⚡ Getting Started

### 1. Clone the Repository

```
git clone https://github.com/your-username/underwriter-gpt.git
cd underwriter-gpt
```

### 2. Create Virtual Environment

```
python -m venv venv
source venv/bin/activate  # Linux / Mac
venv\Scripts\activate     # Windows
```

### 3. Install Dependencies

```
pip install -r requirements.txt
```

### 4. Run the API

```
uvicorn src.api.main:app --reload
```

### 5. Run the App

```
streamlit run app/streamlit_app.py
```

---

## 📈 Roadmap

* [ ] Data cleaning & preprocessing
* [ ] Baseline ML model
* [ ] Model optimization (XGBoost)
* [ ] FAISS similarity search
* [ ] LLM integration (RAG)
* [ ] API development
* [ ] Web UI
* [ ] Deployment

---

## 💡 Future Improvements

* Real-time model monitoring
* Bias and fairness analysis
* Advanced feature engineering
* Multi-model ensemble
* Deployment with scalable infrastructure

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repo and submit a pull request.

---

## 📜 License

MIT License

---

## 👤 Author

Your Name
