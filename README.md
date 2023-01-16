# NLP-Word2vec
# Documentation :

In NLP, word embedding is a term used for the representation of words for text analysis, typically in the form of a real-valued vector that encodes the meaning of the word such that the words that are closer in the vector space are expected to be similar in the meaning.

Word embedding is a technique where you convert a word into a vector

Types of word embedding →

1. Frequency-based (BoW, tf-idf, glove)
2. Prediction-based (Word2vec)

Question. What is word2vec?
Answer. It is a word embedding technique that converts the word into a collection of numbers.
you can not directly apply the algorithm to the word, first, you have to convert it into numbers and then apply the algorithm.

Advantages of using Word2vec →

1. semantic meaning {Happy, Joy}
2. Low-dimension vectors are formed. (100 to 300)
3. Dense Vector (less non-zero vector, which solves the problem of overfitting)

Now understand this with an example:

Suppose you give input to the computer in the form of

[King — Man + Woman] it will provide the output [Queen]

isn’t this super COOL?

Question. How does the computer do this??
Answer. Computer doesn't understand text, they understand numbers. So if there is a way to convert text into numbers, we can make something interesting out of it.

Let’s convert the word ‘King’ into numbers(vector), such that it can represent the word King accurately.

Let’s create some features of King. (Gender, Wealth, Power, Weight, Speak).

Let's give some numbers to these features.
Gender = 1
Wealth = 1
Power = 1
Weight = 0.8
Speak = 1
Now the representation of King would be something like this → [1,1,1,0.8,1]

Let’s do this for Queen also
Gender = 0
Wealth = 1
Power = 0.7
Weight = 0.4
Speak = 1
Now the representation of King would be something like this → [0,1,0.7,0.4,1]

Let’s do this for Man also
Gender = 1
Wealth = 0.3
Power = 0.2
Weight = 0.6
Speak = 1
Now the representation of King would be something like this → [1,0.3,0.2,0.6,1]

Let’s do this for Women also
Gender = 0
Wealth = 0.3
Power = 0.2
Weight = 0.5
Speak = 1
Now the representation of King would be something like this → [0,0.3,0.2,0.5,1]

Let’s do this for Lion also
Gender = 1
Wealth = 0
Power = 0
Weight = 0.3
Speak = 0
Now the representation of King would be something like this → [1,0,0,0.3,0]

And Now if we do [king — Man + Woman]!!


[King — Man + Woman] = Close to Queen
The vector [0,1,1,0.7,1] is close to Queen.

Here we took only 5 vocabularies but in the real world, we will have these numbers in lakhs and it is impossible to create these many features.

Then Neural Network comes into the picture, but here you will know the value not exactly what is the feature.

The underlying assumption of Word2vec is that two words sharing similar contexts also share a similar meaning and consequently
a similar vector representation from the model
