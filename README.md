## sentiment-analysis
This project aims to perform sentiment analysis on text data using Support Vector Classifier (SVC). The data is preprocessed using nltk and spacy libraries, and the model is evaluated based on its accuracy and performance on test data.

Features
Text Preprocessing: Cleaning, tokenization, stopword removal, and lemmatization using nltk and spacy.
Sentiment Analysis: Classifies text as positive, negative, or neutral using SVM.
Hyperparameter Tuning: Fine-tuning C and gamma parameters to improve the model's accuracy.
Confusion Matrix: Visual representation of the model's performance.
New Data Predictions: Predict sentiments for new unseen data.
Real Review Analysis: Sentiment predictions are saved for new customer reviews.
Dataset
The model is trained and evaluated using a CSV dataset with two columns: text and sentiment. The sentiment has three categories:

Positive
Negative
Neutral
The reviews are preprocessed to remove any noise before feeding them to the model.

Libraries Used
numpy
pandas
matplotlib
seaborn
nltk
spacy
sklearn (Support Vector Classifier)
collections
How to Run the Project
Clone the repository:
bash
Copy code
git clone https://github.com/yourusername/sentiment-analysis-svc.git
Install the required libraries:
bash
Copy code
pip install -r requirements.txt
Place the training data (train.csv) and testing data (test.csv) in the root directory.
Run the script:
bash
Copy code
python sentiment_analysis.py
Model Overview
We use the Support Vector Classifier (SVC) from sklearn to build a sentiment analysis model. The model is trained on a labeled dataset, with the text being classified as positive, negative, or neutral.

The following steps are performed in the project:

Data Preprocessing: Text cleaning, tokenization, stopwords removal, and lemmatization.
Model Training: Using SVC to classify text into different sentiments.
Hyperparameter Tuning: Tuning the model's parameters (C and gamma) to improve its accuracy.
Model Evaluation: Confusion matrix, classification report, and accuracy score are calculated.
Sample Results
A sample confusion matrix from the model evaluation is shown below:

mathematica
Copy code
Confusion Matrix:
                  Predicted
                Negative  Neutral  Positive
True Negative      50        8       2
True Neutral       10       70       5
True Positive      3         7      65
Example Usage
Below is an example of how the model classifies new text inputs:

kotlin
Copy code
Input: ["I love this movie!", "This product is terrible.", "The food was delicious.", "This product is alright"]
Output:
- I love this movie! 😃
- This product is terrible. 😞
- The food was delicious. 😃
- This product is alright 😐





