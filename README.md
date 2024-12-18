# Sentiment Analysis Using Naive Bayes Classifier

This project focuses on building a sentiment analysis model using the Naive Bayes Classifier. The dataset, `sentiment_analysis_data.csv`, contains sentences labeled with their respective sentiments. The project also explores the impact of balancing data on model performance using SMOTE.

## Table of Contents

- [Dataset Overview](#dataset-overview)
- [Steps Performed](#steps-performed)
- [Observations](#observations)
- [Conclusion](#conclusion)
- [How to Run](#how-to-run)
- [Future Work](#future-work)

## Dataset Overview

- The dataset consists of sentences labeled with three sentiment classes: positive, negative, and neutral.
- Features:
  - **Sentence**: The text data.
  - **Sentiment**: The label (positive, negative, or neutral).

## Steps Performed

1. **Exploration**:
   - Total number of data points and unique values in sentiments identified.
   - Class distribution analyzed for potential imbalances.

2. **Visualization**:
   - Generated word clouds for positive, negative, and neutral sentiments.

3. **Data Preprocessing**:
   - Split the dataset into features (`X`) and labels (`y`).
   - Used `CountVectorizer` (excluding stop words) to vectorize the sentences.

4. **Model Training**:
   - Split the dataset into training and testing sets (75% training, 25% testing, random state = 5).
   - Trained a Multinomial Naive Bayes Classifier with default parameters.

5. **Evaluation**:
   - Analyzed performance using confusion matrix and classification scores.
   - Observed poor performance on negative sentiments due to class imbalance.

6. **Data Balancing**:
   - Applied SMOTE to balance the dataset.
   - Re-trained the model on the balanced dataset.
   - Improved performance, especially for the negative sentiment class.

## Observations

- Before balancing:
  - The model struggled with predicting negative sentiments due to their underrepresentation.
- After balancing:
  - Improved recall and precision for negative sentiments.
  - The overall performance of the model increased, as reflected in the confusion matrix.

## Conclusion

Balancing the dataset using SMOTE significantly improved the model's ability to classify negative sentiments, addressing the data imbalance issue.

## How to Run

1. Clone the repository and navigate to the project folder.
2. Ensure you have Python installed along with the necessary libraries:
   - `numpy`
   - `pandas`
   - `sklearn`
   - `matplotlib`
   - `wordcloud`
3. Load the dataset (`sentiment_analysis_data.csv`) into Google Colab or your local environment.
4. Execute the steps in the notebook to reproduce the results.

## Future Work

- Explore advanced feature extraction techniques like TF-IDF.
- Experiment with different classifiers (e.g., SVM, Random Forest).
- Incorporate deep learning models for sentiment analysis.
- Perform further hyperparameter tuning for improved performance.
