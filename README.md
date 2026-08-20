# Email Spam Classification Using Perceptron

## Project Overview

This project develops a machine learning model that classifies email messages as either **Spam** or **Ham** using the **Perceptron algorithm**.

The project covers the complete machine learning workflow, including exploratory data analysis, text preprocessing, feature extraction, model training, evaluation, prediction, and model saving.

## Dataset

The dataset contains **193,852 email records** with two main columns:

- `label` - Email category (Ham or Spam)
- `text` - Email message content

The class distribution is approximately:

- Ham: 52.7%
- Spam: 47.3%

## Project Workflow

1. Load and explore the dataset
2. Check missing values and duplicates
3. Perform exploratory data analysis
4. Analyze email length and class distribution
5. Clean and preprocess email text
6. Convert labels to numerical values
7. Split data into training and testing sets
8. Extract text features using TF-IDF
9. Train a Perceptron classifier
10. Evaluate model performance
11. Test the model with new email messages
12. Save and reload the trained model

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Machine Learning Model

The project uses a **Perceptron classifier** with TF-IDF text features.

TF-IDF configuration:

- Maximum features: 10,000
- English stop words removed
- Unigrams and bigrams
- Training/Test Split: 80% / 20%

## Model Performance

| Metric | Score |
|---|---:|
| Accuracy | 97.61% |
| Precision | 97.71% |
| Recall | 97.22% |
| F1 Score | 97.47% |

## Confusion Matrix

The model produced:

- 20,015 correctly classified Ham emails
- 17,829 correctly classified Spam emails
- 417 Ham emails incorrectly classified as Spam
- 510 Spam emails incorrectly classified as Ham

## Prediction Example

The trained model can classify new email messages as Spam or Ham.

Example:

`Win a free iPhone now, click this link`

Prediction:

`Spam`

## Model Deployment

The trained Perceptron model and TF-IDF vectorizer are saved using Python's `pickle` module so they can be loaded later without retraining the model.

## Conclusion

The Perceptron classifier achieved strong performance for email spam detection, reaching approximately **97.61% accuracy** and **97.47% F1 score**.

The project demonstrates how text preprocessing and TF-IDF feature extraction can be combined with a linear classifier to build an effective spam detection system.