# Sentiment Analysis Using Support Vector Classifier (SVC)

This project performs **sentiment analysis** on text data using a **Support Vector Classifier (SVC)**. The data is preprocessed using **nltk** and **spacy** libraries, and the model is evaluated based on accuracy and performance on the test dataset.

## Features

- **Text Preprocessing**: Cleaning, tokenization, stopword removal, and lemmatization using `nltk` and `spacy`.
- **Sentiment Analysis**: Classifies text as **positive**, **negative**, or **neutral** using **SVM**.
- **Hyperparameter Tuning**: Fine-tuning the `C` and `gamma` parameters to improve the model's accuracy.
- **Confusion Matrix**: Provides a visual representation of the model's performance.
- **New Data Predictions**: Predicts sentiments for unseen text data.
- **Real Review Analysis**: Analyzes and predicts sentiment for new customer reviews and saves the predictions.

---

## Dataset

The model is trained and evaluated using a **CSV dataset** containing two columns:
- `text`
- `sentiment`

The **sentiment** column has three categories:
- **Positive**
- **Negative**
- **Neutral**

Before being fed into the model, the text reviews are preprocessed to remove any noise.

---

## Libraries Used

The following Python libraries are used in the project:
- **numpy**
- **pandas**
- **matplotlib**
- **seaborn**
- **nltk**
- **spacy**
- **sklearn** (Support Vector Classifier)
- **collections**

---

## How to Run the Project

Follow the steps below to run the project on your local machine:

1. **Clone the repository**:
```bash
   git clone https://github.com/yourusername/sentiment-analysis-svc.git
Install the required libraries:
```

```bash
pip install -r requirements.txt
```
Place the training and testing data (train.csv and test.csv) in the root directory.

Run the script:

```bash
python sentiment_analysis.py
```
Model Overview
We use the Support Vector Classifier (SVC) from the sklearn library to build a sentiment analysis model. The model is trained on a labeled dataset, with the text being classified as positive, negative, or neutral.

Key Steps
Data Preprocessing:

Text cleaning
Tokenization
Stopwords removal
Lemmatization
Model Training:

Using SVC to classify text into different sentiment categories.
Hyperparameter Tuning:

Tuning the model's C and gamma parameters to improve accuracy.
Model Evaluation:

Generating a confusion matrix, classification report, and calculating the accuracy score.
Sample Results
Here is an example confusion matrix generated from the model evaluation:

mathematica

Confusion Matrix:
                      Predicted
| True \ Predicted | Negative | Neutral | Positive |
|------------------|----------|---------|----------|
| **Negative**      | 50       | 8       | 2        |
| **Neutral**       | 10       | 70      | 5        |
| **Positive**      | 3        | 7       | 65       |

## Example Usage

Below is an example of how the model classifies new text inputs:

##Input:
```python
["I love this movie!", "This product is terrible.", "The food was delicious.", "This product is alright"]
```
##Output:
```python
I love this movie!  😃
This product is terrible.  😞
The food was delicious.  😃
This product is alright.  😐
```
