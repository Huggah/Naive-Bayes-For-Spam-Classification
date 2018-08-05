# Naive Bayes For Spam Classification
This is simple naive bayes classifier, or a classifier using Bayes Theorem to compute probabilities given new data, used to classify messages as either spam or not spam.

Bayes Theorem uses prior knowledge along with collected data to compute the probability of parameters based on data, P(A|B), where what is available is the probability of the data given the parameters, P(B|A). In this case, prior knowledge would be the probability that an email is spam, or P(spam), and collected data would be the probability of certain words appearing in a spam message, or P(words|spam). The dataset used to get this information was the [SMS Spam Collection Dataset](https://www.kaggle.com/uciml/sms-spam-collection-dataset) by Kaggle.

![bayestheorem](http://imagehost7.online-image-editor.com/oie_upload/images/534576G967R8roJ/vjICZXedlz9e.png)

In the case of spam classification, we want to find the frequency of words that are spam and the frequency of all words regardless, and we normalize them to get probabilities, ending up with P(words|spam) and P(words). We can use the probability that any given email is spam as our prior, P(spam), and use a derivation of Bayes Theorem to finding the probability that some given words is spam, finding the joint likelihood and marginal of B for every word.

![jointbayes](https://latex.codecogs.com/png.latex?%5Clarge%20P%28spam%7Cwords%29%20%3D%20P%28spam%29%5Cprod_%7Bk%7D%5Cfrac%7BP%28words_k%7Cspam%29%7D%7BP%28words_k%29%7D)
