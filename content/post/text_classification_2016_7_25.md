+++
author = "xuefeng huang"
date = "2016-07-25"
description = "note about sklearn text classification"
keywords = ["python", "sklearn"]
tags = ["python"]
title = "text classification using sklearn"
type = "post"

+++

I have used scikit-learn module to do text classification recently, here is a summary of each step is doing:  
use CountVectorizer from sklearn to do tokenization, stemming and get the feature  vector of each article (number of times each word appears in the document, this is the bag-of-word model)
```python
count_vect = CountVectorizer(tokenizer=tokenize, stop_words='english', decode_error='replace')

X_train_counts = count_vect.fit_transform(data)
```
use TfidfTransformer from sklearn to do the tf-idf transformation of the feature vector(get calculate word frequency in the document and assign weightage to each word, higher frequency word compare to the frequency in the whole corpora get more weight)  

```python
tfidf_transformer = TfidfTransformer()
X_train_tfidf = tfidf_transformer.fit_transform(X_train_counts)
```
use feature vector abtained above and the labels for each article to train the classifier (used Naive Bayes below)

```python
clf = MultinomialNB(alpha=0.001).fit(X_train_tfidf, label)
```
save the classifier, CountVectorizer and TfidfTransformer to disk for future prediction

```python
from sklearn.externals import joblib

joblib.dump(clf, 'classifier/clf.pkl')
joblib.dump(count_vect, 'vectorizer/vectorizer.pkl')
joblib.dump(tfidf_transformer, 'tfidf/tfidf_transformer.pkl')
```