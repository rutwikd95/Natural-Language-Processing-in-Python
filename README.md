# Natural-Language-Processing-in-Python
Using NLP to classify the data from SMS Spam Collection Dataset (from UCI's datasets) as spam or ham.

This project goes through the following steps:

- Getting the Data:
  - We'll be using a dataset from the UCI datasets which can be found at https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection
  - The file we are using contains a collection of more than 5 thousand SMS phone messages.

- Basic Exploratory Data Analysis:
  - Here, we will check stats and do some plotting eg. plotting lengths of messages based on the labels.
  
- Text Pre-Processing:
  - Split messages into individual words and insert into a list.
  - Using NLTK library, remove the common words.
  
- Vectorization:
  - Converting each of those messages into a vector, the SciKit Learn's algorithm models can work with.
  - We'll do that in three steps using the bag-of-words model:
      - Count how many times does a word occur in each message (Known as term frequency)
      - Weigh the counts, so that frequent tokens get lower weight (inverse document frequency)
      - Normalize the vectors to unit length, to abstract from the original text length (L2 norm)
      
  - Using SciKit Learn's CountVectorizer to convert a collection of text documents to a matrix of token counts.

- Training the Model:
  - With messages represented as vectors, we can finally train our spam/ham classifier. Now we can actually use almost any sort  of classification algorithms. Here, we will be using the Naive Bayes Classifier.
  - Check model accuracy.

- Creating a Data Pipeline
  - Using SciKit Learn's pipeline capabilities, we store a pipline of workflow.
