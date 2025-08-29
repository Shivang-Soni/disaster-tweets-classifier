# Disaster Tweets Classification

This project is based on the Kaggle competition [NLP with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started).  
The goal is to classify tweets as **disaster-related** or **not disaster-related**.

---

## Project Structure

- `Kaggle_disaster_tweets_prediction_model.ipynb` → Main Jupyter Notebook with all steps  
- `train.csv` → Original training dataset  
- `train_clean.csv` → Cleaned training data  
- `test.csv` → Original test dataset  
- `test_clean.csv` → Cleaned test data  
- `results/` → Folder containing model outputs and submission CSV files  
- `get-pip.py` → Script to install pip if missing  
- `README.md` → Project documentation  

---

## Dataset

- Source: [Kaggle - Natural Language Processing with Disaster Tweets](https://www.kaggle.com/competitions/nlp-getting-started)  
- Train set: 7,613 tweets  
- Test set: 3,263 tweets  
- Task: Binary classification (1 = disaster, 0 = not disaster)

---

## Approach

1. **Data Cleaning**  
   - Removed hashtags, mentions, links, emojis, special characters, and numbers  
   - Lowercased text and stripped whitespace  

2. **Feature Engineering**  
   - Tokenization using NLTK / HuggingFace tokenizer  
   - TF-IDF vectorization for baseline model  
   - Word embeddings with BERT/RoBERTa for advanced models  

3. **Models**  
   - Logistic Regression (baseline, ~75% accuracy)  
   - Fine-tuned Transformers (BERT, RoBERTa)

4. **Evaluation**  
   - Train/Test split: 80/20  
   - Metrics: Accuracy, F1-Score  

5. **Predictions**  
   - Predictions saved in `results/` folder for Kaggle submission  

---

## Results

- Logistic Regression (TF-IDF): ~75% accuracy  
- BERT fine-tuned: ~83% accuracy  

---

## How to Run

1. Open the notebook `Kaggle_disaster_tweets_prediction_model.ipynb` in Jupyter.  
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
