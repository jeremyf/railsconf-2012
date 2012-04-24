# Practical Machine Learning and Rails
by Andrew Cantino & Ryan Stout
@tectonic & @ryanstout

## Presentation

- introduce machine learning
- make you ML-aware
- examples

Decision Tree Learning

Support Vector Machines
	Find a line that maximizes the margin that separates good vs. bad
	require 'libsvm'

Naive Bayes
	Effective on text

Neural Nets
	Warn aware from them, as SVM is easier to maintain
	
The more features you have the more data you need.

Generalize not memorize

Know what your biases are before you can assume your machine has learned

### Sentiment Classification/Analysis

Is it positive or negative 

Training Data:
- tweets
- positive/negative
	- use emoticons from twitter

Bag of Words Model
	split the text, create dictionary, replace text with word counts

WEKA – contains common ML algorithms
can access it from jRuby

correctly classified
mean squared error

unbalanced data needs to review Confusion Matrix

### Sentiment Classification Example
http://github.com/ryanstout/mlexample

bi-grams/tri-grams

### Feature Generation

think about what information is valuable to an expert
remove data that isn't useful (attribute selection)

### Domain Price Prediction

predict how much a domain would sell for

* collaborative filtering
* cluster - unsupervised learning

## Takeaway

Weka is a powerful Java tool…and can be accessed via jRuby.
Write a reputation monitoring script for ND
ml-class.org - Stanford machine learning class

http://github.com/paulasmuth/recommendify – Collaborative filter 