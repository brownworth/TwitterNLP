# TwitterNLP
Implementation of the Word2Vec Word Embeddings trained on time-constrained small corpora of Twitter tweets.

## Summary
The Jupyter notebook contained in this repository contains a proof of concept for scoring a set of tweets based upon their relatedness to a single search term. The algorithm uses an implementation of the Word2Vec developed by Mikolov, et al, to create word embeddings based upon a small corpus of tweets. By training a neural network on a small, time-constrained corpus of tweets, rather than a large comprehensive set of corpora, the objective is to derive relative meaning from changing context. 

## Functionality
The associated code does the following:
- Import a set of tweets from a .csv file, formatted to include the text of the tweets, data for encoded language, and date of composition. The functions tolerate additional data for potential associated analysis (e.g. geospatial data, user, etc.)
- Separate tweets by date
- Clean text: remove case, URLs, @mentions, non-hashtag punctuation, non-hashtag '#', encoded HTML, non-hashtag numbers, remove repeated characters in excess of three
- Defines four vector comparison functions:
- - Mean Cosine Similarity
- - Sum Cosine Similarity Over Square Root of Length
- - Dot Product of 'Tweet As Matrix Sum of Term Vectors' and 'Search Term'
- - Cosine Similarity of 'Tweet As Matrix Sum of Term Vectors' and 'Search Term'
- Train the Word2Vec Neural Network on cleaned tweets
- Score tweets based upon their relatedness to a search term using each of the four operations above.

Additionally, the code generates visualizations based upon the cleaning operations, human-encoded tweets, and distributions of tweet counts by hour.
