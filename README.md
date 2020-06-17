# Fake-News-Classifier
I downloaded a data set which was available online for free. I trained the model on the data set and tested it on the test set. Simple right? Yeah! But not so easy. At least not for me! I used Naïve Bayes Classifier to, umm well, classify the news into two groups- Fake, and Not Fake.
Dataset used:

I used the “Liar, Liar Pants on Fire”: A New Benchmark Dataset for Fake News Detection, which is available online. It contains files in .tsv (Tabs Separated Values) format. 
First I used CountVectorizer. CountVectorizer counts the frequencies of the words. Period!

Counting the words is all fine and okay, but there is a problem with that. Words like “the”, “a”,… which do not hold any special meaning to the context of the sentence gets also counted, ergo their meaning will also be not very meaningful in the encoded vectors.

One alternative solution to this is TF-IDF.

TF-IDF are word frequency scores that tries to highlight the words that are more interesting to us (more meaningful). With the TF-IDF vectorizer, the value increases with the count of the words, but is offset by the frequency of the word in the corpus i.e. words frequent in a document but not across the documents (that is  why the “inverse document frequency” is used).

Now that EDA and feature engineering has been done, now comes the most awaited part – fitting the machine learning model to the training set and testing it on the test set. I used Naïve Bayes Classifier. I am not going into the math behind this particular ML model, because it is beyond the scope of this article. I trained and tested it, and the accuracy of my model came out to be 77.65%.

Not so bad right!
