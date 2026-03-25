# SENTIMENT-ANALYSIS-OF-AMAZON-SALES-DATA-REVIEWS

# Overview
This project uses sentiment analysis model through Natural Language Processing (NLP) techniques to classify Amazon product reviews as either positive or negative.
The workflow imitates the sentiment classification pipeline demonstrated in class (using the IMDB dataset) but applies it to a product review dataset, as required by the assignment.
The project follows a complete NLP pipeline including data loading, text preprocessing, exploratory text analysis, feature extraction using TF-IDF, model training, evaluation, and testing.
Dataset Description
The dataset consists of Amazon product reviews already split into two CSV files:
amazon_train.csv – training data
amazon_test.csv – testing data

And each dataset contains the following columns:

1. label: Sentiment label where 0 = Negative, and 1= Positive
2. title: Review title
3. review: Full review text
4. review_length_chars: which is the Number of characters in the review
5. review_length_words: Number of words in the review
6. clean_review: Preprocessed review text

Through a bar graph, the dataset was. discovered to be balanced, containing approximately equal numbers of positive and negative reviews. Which means low chances of the model being trained on skewed data hence favoring one of the two classes.

# Methodology / NLP Pipeline

1. Data Loading
Training and testing datasets are loaded separately from CSV files. The links for these datasets are below:



And the predefined train/test split is preserved to avoid data leakage.

2. Exploratory Data Analysis (EDA)
Review length statistics (characters and words) were computed.
Histograms were plotted to visualize the distribution of review lengths.
This helped identify skewness and variability in review sizes.
3. Text Preprocessing
A custom text cleaning function was applied to both datasets, performing:
-Conversion to lowercase
-Removal of HTML tags
-Removal of punctuation
-Removal of numbers
-Removal of extra whitespace
The cleaned text was stored in a new column: clean_review.
4. Feature Extraction (TF-IDF)
Text data was converted into numerical features using TF-IDF Vectorization
Parameters:
Stop words: English
Maximum features: 5,000

The vectorizer was fit only on training data and applied to test data to prevent information leakage.

6. Model Training
Logistic Regression was used as the classification model.
The model was trained on TF-IDF features extracted from the training dataset.
7. Model Evaluation
The model was evaluated on the test dataset using:
Accuracy
Precision
Recall
F1-score
Classification report
8. Results
Model Performance:
Accuracy: ~86%
Balanced precision and recall for both sentiment classes
Strong and stable performance across positive and negative reviews
This demonstrates that the model generalizes well and successfully captures sentiment patterns in product reviews.
9. Tools Used
Python
Pandas & NumPy – data handling
NLTK & Regex – text preprocessing
Scikit-learn
TF-IDF Vectorizer
Logistic Regression
Evaluation metrics
Matplotlib & Seaborn – data visualization
Jupyter Notebook

# How to Run The Project

1. Ensure Python 3 is installed
2. Download the project and the used CSVs
3. Open the notebook
   jupyter notebook nlp_model.ipynb
4. Run all cells

# AUTHOR
Amaranth Sebeo Madise
