# fractal_ml_casestudy

## Project Overview & Workflow

### 1. Problem Statement
- Predict the subject/category of a text sample (multi-class classification)
- Dataset: Real-world, noisy, unstructured text

### 2. Data Exploration & Preprocessing
- Loaded train and test CSVs
- Explored class distribution, sentence length, and frequent words
- Cleaned text: lowercasing, HTML removal, stopword removal, lemmatization
- Visualized class overlap and word clouds

### 3. Modeling Approaches
- **Baseline:** TF-IDF + Logistic Regression (scikit-learn Pipeline)
  - Used n-grams, sublinear TF, class_weight='balanced'
  - Evaluated with macro F1 and classification report
- **Advanced:** BERT-based Sequence Classification (HuggingFace Transformers)
  - Used robust text cleaning, BERT tokenizer, stratified train/val split
  - Trained with Trainer API, macro F1 metric, and hyperparameter tuning

### 4. Model Training & Evaluation
- Baseline: Fast, interpretable, good for benchmarking
- BERT: Higher accuracy with more data and tuning
- Checked prediction distribution and sample outputs for errors

### 5. Submission
- Generated submission file in required format for test set
- Saved as `submission.csv` in results folder

### 6. Key Learnings & Next Steps
- Text cleaning and preprocessing are critical for both classical and deep models
- BERT outperforms baseline with sufficient data and compute
- Next: Try more epochs, tune max_length, ensemble models, or use external data