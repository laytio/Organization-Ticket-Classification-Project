# Ticketing System Text-Based Classifier

## 1. Introduction
The objective of this project is to classify ticketing system data using a text-based machine learning classifier. The dataset is unlabeled, and the labels are derived from the "Request Detail" and "Notes" features. The dataset includes both English and Arabic content, making it a bilingual classification task.

## 2. Preprocessing

### 2.1 Data Cleaning
- **Text Cleaning**: We removed unnecessary elements such as email signatures, disclaimers, punctuation, and stopwords (for both English and Arabic). The text was normalized and tokenized.
- **Tokenization**: The text was split into individual words using `nltk`'s tokenization functions.
- **Stopwords Removal**: English and Arabic stopwords were removed from the data.

### 2.2 Exploratory Data Analysis (EDA)
- **Word Frequency Analysis**: A word cloud was generated to visualize the most frequent terms in the "Request Detail" feature.
- **Distribution of Text Lengths**: The distribution of text lengths in the "Request Detail" field was analyzed.
- **Correlation Matrix**: A correlation matrix was visualized to show relationships between text features like length and word count.

## 3. Feature Engineering
- **New Features**: We created new features such as text length, word count, and presence of technical issue keywords.
- **Dimensionality Reduction**: We applied PCA to reduce the dimensionality of the numeric features.

## 4. Label Extraction
Two types of labels were derived from the text using keyword-based classification:
- **Technical Issue**: Extracted based on the presence of keywords like "error," "fail," etc.
- **Service Request**: Extracted from keywords like "request," "service," etc.

## 5. Modeling

### 5.1 Classifiers Used
Three classifiers were trained and evaluated:
1. **Random Forest**: A robust classifier for text features.
2. **SVM**: A support vector machine with a linear kernel.
3. **Transformers**: A BERT-based model for sequence classification.

### 5.2 Model Tuning
Hyperparameters were tuned for each classifier to achieve the best performance.

## 6. Evaluation
We evaluated the models using three key metrics:
- **Accuracy**: Proportion of correct predictions.
- **Precision**: Measure of exactness.
- **Recall**: Measure of completeness.

Based on the results, the Random Forest model performed the best, achieving the highest accuracy and recall.

## 7. Conclusion
This project involved building a bilingual text classifier using both traditional and modern NLP techniques. The results show that a Random Forest model with TF-IDF features is effective for this task.

## 8. Future Work
- Explore more advanced transformers for better accuracy.
- Experiment with stacking classifiers to further improve performance.

