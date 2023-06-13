# Make a model which can check the profanity in a sentence and remove those words with **#####**

## Data Collection: for collecting data used towardsDataScience article.
## DataLink: https://towardsdatascience.com/building-a-better-profanity-detection-library-with-scikit-learn-3638b2f2c4c2

## Libraries and Packages:
Pandas

Numpy

Sklearn - CountVectorizer

NLTK

Better Profanity for Profanity Check

## Steps Involved:
## 1. Data Collection and Loading the Data
## 2. Pre-Processing the Data
## 3. Extracted rows from Data for furthur Process
## 4. Splitting the Data in to train and test
## 5. CountVectorizer
## 6. Building and Fitting the Model
## 7. Predicting the Model
## 8. BetterProfanity Installation for Profanity check
## 9. Final output
## 8. Evaluating Metrics - Accuracy, F1 Score, AUROC.

**Explanation:** Collected Data contains above one lakh rows with 2 columns.i.e. Is_offensive, text. Data contains unneccesary information like smileys, numbers and all. 
cleaned the data by importing ntlk libraries and removed all punctuations, smileys, etc.
Dataset is very large. Not possible to train all rows. For time being extracted 10000 rows from the dataset for furthur process.

Splitted the data into train and test for building the model. CountVectorizer class is imported from scikit-learn's sklearn.feature_extraction.text module. 
This object will be used to convert the input text data into a count matrix representation. The fit_transform() method of the CountVectorizer object is used to convert 
the input data x into a count matrix. The fit_transform() method performs two main actions:

1> Fitting: During the fit() step, the CountVectorizer analyzes the input text data to learn the vocabulary and build the necessary data structures.

2> Transforming: After fitting, the transform() step takes place. The transform() method converts the input text data into a count matrix representation based on the 
learned vocabulary.

Building and fitted the DecisionTreeClassifier Model and predicted the test data. got **80%** F1 Score and **87%** Auroc Score and plotted the confusion matrix and roc
plot. The next step is to check profanity. for this used better profanity from profanity check and created function to remove profanity check. Applied to all 10000 rows 
in the dataset. Got the final output. The bad words are removed and replaced with '#'.
