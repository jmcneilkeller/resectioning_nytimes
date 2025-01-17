# Resectioning the NY Times

## 1. The question

Are the categories by which the NY Times sorts it's online articles still meaningful, or are there other latent groupings which would better recommend like articles to readers?

## 2. The data

* 10,700 articles taken as snapshots from the NYTimes landing page from archive.org between 2014 and 2018.
* Uncategorized but tagged with persistent URLs.
* Majority of articles were classified as US/Politics in the URL.

## 3. The process

* The article texts were passed through a spaCy pipeline to tokenize, tag, lemmatize and remove stopwords.
* Custom stopwords were added to remove common repeats like titles, byline locations, etc...
* The resultant text was run through Gensim's Latent Dirichlet Allocation for topic modeling.

![](https://github.com/jmcneilkeller/Resectioning_the_NYTimes/blob/master/img/More_topics.png)

## 4. The results

* Selected 32 topics as the optimal number based on parameter tuning of the LDA model.
* Best coherency score: 0.58
* Final sample topics: 

![](https://github.com/jmcneilkeller/Resectioning_the_NYTimes/blob/master/img/Topic_word_counts_weights.png)
