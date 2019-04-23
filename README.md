# Project Proposal - IMDB Movie Sentiment
Prepared for: Annie Lee, PHD, MMATH
Prepared by: Jairo Melo, Ing. MSC
March 27, 2019
Proposal number: ML1010-IMDB001

## 1. Problem Definition
Sentiment analysis is a well-known method in the world of natural language processing. The  objective is to determine the polarity of of the reviews.  The inputs the Movie reviews collected by IMDB, and the output is whether the review is positive or negative.

## 2. Dataset
This is a dataset for binary sentiment classification.  The IMDB dataset provides a set of 25,000 highly polar movie reviews for training, and 25,000 for testing. There is additional unlabeled data for use as well. Raw text and already processed bag of words formats are provided.
http://ai.stanford.edu/~amaas/data/sentiment/
The labeled data set consists of 50,000 IMDB movie reviews, specially selected for sentiment analysis. The sentiment of reviews is binary, meaning the IMDB rating < 5 results in a sentiment score of 0, and rating ≥7 have a sentiment score of 1. No individual movie has more than 30 reviews. The 25,000 review labeled training set does not include any of the same movies as the 25,000 review test set. In addition, there are another 50,000 IMDB reviews provided without any rating labels.


## 3. Data Cleaning and Data Exploration
Remove HTML characters
Tokenize and remove stop words

## 4. Feature Engineering
Lenght of the review
Percentange of punctuation for each review
Number of words
No Stop words: A a feature also called clean text
We use word embedding TF-IDF to vectorize and identify additional features.
Finally, we will use Flair Embeddings to create contextualized word embeddings so we can feed these embeddings to our model.

## 5. Project First Milestone
We chose three algorithms for Text Classification: Model Random Forest, Gradient Boosting and Flair NLP State of the Art.  We evaluated performance, accuracy, precision, recall, and score.  All three are great algorithms but only one showed the best performance and accuracy.

Training Random Forest Model
Random forest shows a great performance fitting the model as well as predicting.  The features importance start with the length, punctuation and tokenized text.

Training Gradient Boosting Model
Fitting and Predicting is very expensive.  The feature considered are only Punctuation and Tokenized words.  Word count and Length are disregarded.  

Random forest and Gradient Boosting Model Evaluation
As shown in the charts, both models have great skill of learning and good precision curve which both have great predicting power.  However, based on performance, accuracy and precision we conclude Random Forest is the selected model from these two.


Flair Text Classifier
We trained a Flair Text classifier Model 150 epochs during two days; Accuracy of 47% and F1 Score of 65%.


Conclusion: Random Forest is our best predicting model based on our initial criteria:


Acknowledge
https://github.com/google/eng-edu/tree/master/ml/guides/text_classification
https://github.com/zalandoresearch/flair/tree/master/resources/docs
