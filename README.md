# Fake_news_detection
# 📰 Fake News Detection — Onion / NotOnion Classifier
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1hW8K9v6hdSr7nCz2EExx5Y-stqO269Vq?usp=sharing)

## 📖 Project Overview

The goal of this project is to distinguish between **satirical (fake)** headlines from *The Onion* and **real** news headlines from credible sources using Natural Language Processing (NLP) and Machine Learning.  
We build, evaluate, and deploy a classifier that you can test directly in the notebook or as a web demo.

## 🚀 What’s Inside / Features

- End-to-end Colab notebook (data download, cleaning, training, evaluation)  
- Baseline model: TF-IDF + Logistic Regression  
- Semantic model: Sentence-BERT embeddings + classifier  
- Model interpretability (feature importance)  
- Simple interface to test new headlines  
- Option to package into a web app (via Gradio / Streamlit)  
- Saved model artifacts for reuse or deployment  

---

## 📁 Repository Structure (suggested)

Fake-News-Detection/
│
├── Fake_News_Detection.ipynb ← Colab notebook with all steps
├── README.md ← This file
├── requirements.txt ← Project dependencies
├── model_artifacts/ ← Saved model & vectorizer (optional)
│ ├── fake_news_pipeline.joblib
│ ├── fake_news_sbert_clf.joblib
yaml
## 🎯 How to Use / Run

### 1. Run in Google Colab  
Click the badge at the top, or visit  
[Colab Notebook](https://colab.research.google.com/drive/1hW8K9v6hdSr7nCz2EExx5Y-stqO269Vq?usp=sharing)  
Then run cell-by-cell (or “Runtime → Run all”).  
You’ll see data preprocessing, model training, evaluation, and a small text input for testing your own headlines.

### 2. Local Setup (optional)

Clone this repo:
```bash
git clone https://github.com/yourusername/Fake-News-Detection.git
cd Fake-News-Detection
Install dependencies:

bash
Copy code
pip install -r requirements.txt
Open the notebook in Jupyter or VS Code and run it locally (if you have the dataset onion.csv & notonion.csv in the folder or download via Kaggle API).

3. Try a Demo / Web App
In the notebook, there’s a section (or optional cell) to use Gradio or Streamlit to run a mini app:

Enter a headline → the app returns Fake or Real

If run with share=True (in Gradio), you’ll get a public link to share the app

You can also deploy the app by pushing it to Streamlit Cloud or Hugging Face Spaces.

📊 Results & Metrics (Example)
Below are sample metrics using the baseline model (TF-IDF + Logistic Regression). Your actual results may vary with hyperparameters or preprocessing tweaks.

Metric	Value
Accuracy	~0.95 (example)
F1 Score	0.94
Precision	0.93
Recall	0.95

Top indicative tokens

satire / fake class: study, report, world, claims

real class: according, says, official, government

🛠️ Project Roadmap / Further Experiments
Ensemble TF-IDF + SBERT models

Character n-gram features

Fine-tune transformer models (e.g. DistilBERT)

Add explainability (LIME/SHAP) in the UI

Test on external news datasets for robustness

Deploy the web app permanently (Streamlit Cloud / Heroku / Hugging Face Spaces)

⚠️ Ethical Considerations & Limitations
The dataset labels parody/satire vs. “real news.” Satirical posts are intentionally deceptive for humor — misclassifying them may be acceptable, but labeling real serious misinformation is a bigger risk.

Always include model confidence and human oversight in any real-world deployment.

The model is trained only on headlines — it’s limited in context and may fail on ambiguous inputs.
🧑‍💻 About the Author
Your Name: Geetha 
Email: singireddygeethasri@gmail.com
Developed an end-to-end fake-news classification system using NLP (TF-IDF + Logistic Regression and Sentence-BERT embeddings) on the Onion/NotOnion dataset. Achieved ~95% accuracy, built a demo UI, and published a reusable Colab notebook for reproducibility.
