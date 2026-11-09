Banking Intent Classification | NLP & Machine Learning
Status: In progress
Tech: Python, Pandas, scikit-learn, TF-IDF, Logistic Regression, Git

Overview
A natural language processing (NLP) and machine learning (ML) project that classifies banking customer messages into 77 intent categories. The goal is to help identify the type of support a customer needs, such as card delivery, transfers, or payment issues.
Dataset
BANKING77 provides 10,003 training messages and 3,080 held-out test messages. I split the original training data into 8,002 training and 2,001 validation messages, preserving the distribution of intent labels.

NLP & Modeling Workflow
1. Explore and clean text: Used Python and Pandas to inspect the dataset, review possible spelling errors in context, and preserve meaningful banking terms and negations.
2. Extract text features: Used TfidfVectorizer for tokenization and TF-IDF weighting, including unigrams and bigrams to capture individual words and short phrases.
3. Train an ML model: Built a scikit-learn Pipeline combining TF-IDF with multiclass Logistic Regression. The vectorizer learns from training data only, reducing the risk of preprocessing leakage.
4. Evaluate: Measured validation accuracy, precision, recall, and F1-score across the 77 intent classes.
Baseline Results
Metric	Validation result
Accuracy	84%
Macro F1-score	0.84
Validation messages	2,001


Next Steps
- Investigate misclassified messages and frequently confused intents.
- Test targeted improvements against the baseline.
- Evaluate the final selected model on the held-out test set.
Notebook: [`notebooks/01_eda.ipynb`](notebooks/01_eda.ipynb)