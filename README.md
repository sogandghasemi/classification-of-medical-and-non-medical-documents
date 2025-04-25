
# Medical vs Non-Medical Document Classifier

## Introduction

This project classifies documents as medical or non-medical using Wikipedia-sourced data and machine learning techniques. It extracts keywords, processes documents, and uses a classifier to determine the category of the documents. The model is tested on real-world documents and evaluated using accuracy.

## Workflow

1. **Topic Selection**  
   Sampled annotated keywords from Wikipedia are used to define topics for both medical and non-medical categories.

2. **Keyword Extraction**  
   Common words, especially nouns, are extracted from the documents using NLTK. These nouns serve as features for the classification model.

3. **Data Preprocessing**  
   Wikipedia API is used to fetch the content, and natural language processing techniques are used to clean and tokenize the text.

4. **Feature Extraction**  
   A `CountVectorizer` is employed to convert the most frequent nouns into numerical features.

5. **Model Training**  
   Two classifiers are used:
   - **Majority Class Naive Classifier** – Predicts the majority class.
   - **Logistic Regression** – Provides a more accurate classification model.

6. **Testing with PDF**  
   A sample medical document in PDF format is tested with the classifier, and the model accurately identifies whether the document is medical or non-medical.

## Requirements

- Python 3.x
- `wikipedia-api`
- `nltk`
- `sklearn`
- `PyPDF2`
- `matplotlib`
- `pandas`

Install dependencies using:

```bash
pip install wikipedia-api nltk scikit-learn PyPDF2 matplotlib pandas
```

## File Structure

- `medical_docs/` - Medical-related documents from Wikipedia.
- `non_medical_docs/` - Non-medical-related documents from Wikipedia.
- `classifier.py` - Contains the logic for training and testing the classifier.
- `sample_document.pdf` - Sample medical document for testing.
  
## Code Overview

1. **Getting Wikipedia Text**  
   The function `get_wikipedia_text` fetches the text content of a given Wikipedia page using the Wikipedia API.

2. **Extracting Keywords and Nouns**  
   `extract_keywords` and `extract_nouns` functions process the text to extract the most common nouns, filtering out stop words.

3. **Classifiers**  
   - **Naive Classifier**: A simple Majority Class classifier that predicts the most frequent class in the training data.
   - **Logistic Regression**: A robust classifier used for more accurate classification.

4. **Model Evaluation**  
   The accuracy of the classifiers is evaluated using accuracy scores and classification reports.

5. **Testing with a PDF**  
   The model can classify a medical document converted from a PDF format into text.

## Conclusion

This project demonstrates a simple yet effective approach to text classification using natural language processing and machine learning techniques. The classifier can distinguish between medical and non-medical documents with decent accuracy.

## References

- NLTK documentation: https://www.nltk.org/
- Wikipedia API documentation: https://wikipedia-api.readthedocs.io/
- PyPDF2 documentation: https://pythonhosted.org/PyPDF2/

## File Details

- `classifier.py`: Contains the classification logic and model definitions.
- `sample_document.pdf`: A sample medical document used to test the classifier.
