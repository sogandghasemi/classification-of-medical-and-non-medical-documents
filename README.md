# 🏥 Medical vs Non-Medical Document Classifier

## Introduction

This project focuses on classifying documents as medical or non-medical. It uses Wikipedia APIs to source content, extracts keywords and common terms, and trains a classifier using those features.

## Workflow

1. **Topic Selection**  
   Sampled annotated keywords are used to define topics. Wikipedia APIs fetch relevant documents for each category.

2. **Feature Extraction**  
   Common words are identified from both medical and non-medical documents. These words are used as features in a `CountVectorizer`.

3. **Model Training**  
   A **Majority Class Naive Classifier** is implemented to classify the documents based on the extracted features.

4. **Model Evaluation**  
   A sample PDF (sourced from Wikipedia) is used to test the performance of the classifier.

## Requirements

- Python 3.x  
- `wikipedia-api`  
- `scikit-learn`  
- `PyPDF2`  
- `nltk`  

Install dependencies using:

```bash
pip install wikipedia-api scikit-learn PyPDF2 nltk
```

## File Structure

- `medical_docs/` - Fetched medical documents  
- `non_medical_docs/` - Fetched non-medical documents  
- `classifier.py` - Contains the classifier logic  
- `test_sample.pdf` - Sample file used for evaluation  

## Conclusion

This assignment demonstrates basic text classification using simple NLP techniques and Wikipedia-sourced data. It also highlights the effectiveness of basic classifiers in handling domain-specific document categorization.
