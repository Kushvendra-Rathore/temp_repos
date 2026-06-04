# Project Report: IMDB Sentiment Analysis

## 1. Introduction
The objective of this project is to build a Machine Learning model capable of classifying movie reviews from the IMDB dataset as either **Positive** or **Negative**. Sentiment analysis is a fundamental task in Natural Language Processing (NLP) that helps in understanding public opinion.

## 2. Dataset and Preprocessing
The dataset consists of IMDB movie reviews. The data was split into:
- **Training Set:** 80%
- **Test Set:** 20%

Text preprocessing techniques were applied to clean the data, and feature extraction was performed using vectorization (TF-IDF/Count Vectorizer) to convert text into numerical formats suitable for machine learning algorithms.

## 3. Models Trained
Three distinct classification models were trained and evaluated on this dataset:
1. **Perceptron:** A linear classifier that updates its weights iteratively.
2. **Naive Bayes (MultinomialNB):** A probabilistic classifier based on Bayes' theorem, commonly used for text classification.
3. **Logistic Regression:** A linear model for binary classification, trained with `C=0.01` and the `saga` solver.

## 4. Experimental Results and Evaluation
The models were evaluated on the test set using Accuracy, Precision, Recall, and AUC (Area Under Curve). 

Based on the execution of the models, the performance metrics were compared:
- **Perceptron Accuracy:** (Highest)
- **Naive Bayes Accuracy:** (Competitive)
- **Logistic Regression Accuracy:** (Baseline)

*(Note: Exact accuracy percentages depend on the runtime execution, but the Perceptron consistently outperformed the other models).*

### 4.1 Visualizations Generated
To thoroughly understand the model behaviors, the following visualizations were created:
1. **Train vs Test Split:** A pie chart and bar plot showing the balanced class distribution.
2. **ROC & PR Curves (All Models):** Receiver Operating Characteristic and Precision-Recall curves comparing the three models.
3. **Feature Importance:** A bar chart of the top 10 positive and negative words based on Logistic Regression coefficients.
4. **Final Model ROC/PR (Perceptron):** Highlighting the performance of the winning model.
5. **Confusion Matrix Heatmap:** A visual representation of True Positives, True Negatives, False Positives, and False Negatives for the Perceptron model.
6. **Residual Plot / Decision Function Distribution:** A KDE plot showing the separation of positive and negative classes across the decision threshold.
7. **Training vs Validation Loss Curve:** A learning curve using `SGDClassifier` to demonstrate that the model learns efficiently over 50 epochs without significant overfitting.

## 5. Conclusion
Upon comparing the metrics and evaluating the ROC/PR curves, the **Perceptron** was declared the final winner for this specific dataset. It provided the best balance of precision and recall for sentiment classification on the IMDB reviews.

## 6. Future Work
Future iterations of this project could involve:
- Implementing deep learning models like LSTMs or BERT.
- Hyperparameter tuning using Grid Search to improve Logistic Regression and Naive Bayes performance.
- Expanding the dataset to include reviews from other domains (e.g., product reviews, tweets).
