	What are the different types of Naive Bayes models, such as Gaussian, Multinomial, and Bernoulli?

Naive Bayes classifiers are a collection of classification algorithms based on Bayes’ Theorem. It is not a single algorithm but a family of algorithms where all of them share a common principle, i.e. every pair of features being classified is independent of each other. To start with, let us consider a dataset.

One of the most simple and effective classification algorithms, the Naïve Bayes classifier aids in the rapid development of machine learning models with rapid prediction capabilities.

Naïve Bayes algorithm is used for classification problems. It is highly used in text classification. In text classification tasks, data contains high dimension (as each word represent one feature in the data). It is used in spam filtering, sentiment detection, rating classification etc. The advantage of using naïve Bayes is its speed. It is fast and making prediction is easy with high dimension of data.

This model predicts the probability of an instance belongs to a class with a given set of feature value. It is a probabilistic classifier. It is because it assumes that one feature in the model is independent of existence of another feature. In other words, each feature contributes to the predictions with no relation between each other. In real world, this condition satisfies rarely. It uses Bayes theorem in the algorithm for training and prediction


---------------
Naive Bayes classifiers are a family of simple yet effective probabilistic classifiers based on Bayes' Theorem with a strong (naive) assumption of independence between the features. There are several types of Naive Bayes models, each tailored to different types of data. The most common types are Gaussian Naive Bayes, Multinomial Naive Bayes, and Bernoulli Naive Bayes.


![](Pasted%20image%2020240528213108.png)
![](Pasted%20image%2020240528213144.png)

![](Pasted%20image%2020240528213158.png)

### Summary of Differences

|Aspect|Gaussian Naive Bayes|Multinomial Naive Bayes|Bernoulli Naive Bayes|
|---|---|---|---|
|**Data Type**|Continuous|Discrete (counts/frequencies)|Binary (presence/absence)|
|**Distribution Assumed**|Normal (Gaussian)|Multinomial|Bernoulli|
|**Feature Representation**|Real-valued numbers|Count vectors|Binary vectors|
|**Applications**|Iris dataset, medical data|Text classification (e.g., spam detection)|Text classification with binary features|

### Conclusion

Each type of Naive Bayes model is tailored to different kinds of data and assumes a different underlying distribution for the features. Gaussian Naive Bayes is used for continuous data, Multinomial Naive Bayes for count data, and Bernoulli Naive Bayes for binary data. Choosing the appropriate model depends on the nature of your data and the problem you are trying to solve.


---------------------

Naïve Bayes is also known as a probabilistic classifier since it is based on Bayes’ Theorem. It would be difficult to explain this algorithm without explaining the basics of Bayesian statistics. This theorem, also known as Bayes’ Rule, allows us to “invert” conditional probabilities. As a reminder, conditional probabilities represent the probability of an event given some other event has occurred, which is represented with the following formula: 

![Conditional probability formula](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/c5/88/Conditional_Probability.png)

Bayes’ Theorem is distinguished by its use of sequential events, where additional information later acquired impacts the initial probability. These probabilities are denoted as the prior probability and the posterior probability. The prior probability is the initial probability of an event before it is contextualized under a certain condition, or the marginal probability. The posterior probability is the probability of an event after observing a piece of data. 

A popular example in [statistics and machine learning literature](https://www.stat.cmu.edu/~brian/463-663/week09/Chapter%2003.pdf) (link resides outside ibm.com) to demonstrate this concept is medical testing. For instance, imagine there is an individual, named Jane, who takes a test to determine if she has diabetes. Let’s say that the overall probability having diabetes is 5%; this would be our prior probability. However, if she obtains a positive result from her test, the prior probability is updated to account for this additional information, and it then becomes our posterior probability. This example can be represented with the following equation, using Bayes’ Theorem: 

![Conditional probability formula for diabetes and testing example](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/1a/49/Bayes_Theorem_Example.png)

However, since our knowledge of prior probabilities is not likely to exact given other variables, such as diet, age, family history, et cetera, we typically leverage probability distributions from random samples, simplifying the equation to P(Y|X) = P(X|Y)P(Y) / P(X)


  

What are Naïve Bayes classifiers?

The Naïve Bayes classifier is a supervised machine learning algorithm that is used for classification tasks such as text classification. They use principles of probability to perform classification tasks.

Naïve Bayes is part of a family of generative learning algorithms, meaning that it seeks to model the distribution of inputs of a given class or category. Unlike discriminative classifiers, like logistic regression, it does not learn which features are most important to differentiate between classes.

A brief review of Bayesian statistics

Naïve Bayes is also known as a probabilistic classifier since it is based on Bayes’ Theorem. It would be difficult to explain this algorithm without explaining the basics of Bayesian statistics. This theorem, also known as Bayes’ Rule, allows us to “invert” conditional probabilities. As a reminder, conditional probabilities represent the probability of an event given some other event has occurred, which is represented with the following formula: 

![Conditional probability formula](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/c5/88/Conditional_Probability.png)

Bayes’ Theorem is distinguished by its use of sequential events, where additional information later acquired impacts the initial probability. These probabilities are denoted as the prior probability and the posterior probability. The prior probability is the initial probability of an event before it is contextualized under a certain condition, or the marginal probability. The posterior probability is the probability of an event after observing a piece of data. 

A popular example in [statistics and machine learning literature](https://www.stat.cmu.edu/~brian/463-663/week09/Chapter%2003.pdf) (link resides outside ibm.com) to demonstrate this concept is medical testing. For instance, imagine there is an individual, named Jane, who takes a test to determine if she has diabetes. Let’s say that the overall probability having diabetes is 5%; this would be our prior probability. However, if she obtains a positive result from her test, the prior probability is updated to account for this additional information, and it then becomes our posterior probability. This example can be represented with the following equation, using Bayes’ Theorem: 

![Conditional probability formula for diabetes and testing example](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/1a/49/Bayes_Theorem_Example.png)

However, since our knowledge of prior probabilities is not likely to exact given other variables, such as diet, age, family history, et cetera, we typically leverage probability distributions from random samples, simplifying the equation to P(Y|X) = P(X|Y)P(Y) / P(X)

The return to Naïve Bayes

Naïve Bayes classifiers work differently in that they operate under a couple of key assumptions, earning it the title of “naïve”. It assumes that predictors in a Naïve Bayes model are conditionally independent, or unrelated to any of the other feature in the model. It also assumes that all features contribute equally to the outcome. While these assumptions are often violated in real-world scenarios (e.g. a subsequent word in an e-mail is dependent upon the word that precedes it), it simplifies a classification problem by making it more computationally tractable. That is, only a single probability will now be required for each variable, which, in turn, makes the model computation easier. Despite this unrealistic independence assumption, the classification algorithm performs well, particularly with small sample sizes.

With that assumption in mind, we can now reexamine the parts of a Naïve Bayes classifier more closely. Similar to Bayes’ Theorem, it’ll use conditional and prior probabilities to calculate the posterior probabilities using the following formula: 

![Posterior probability formula](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/9f/c8/Naive_Bayes_Formula.png)

Now, let’s imagine text classification use case to illustrate how the Naïve Bayes algorithm works. Picture an e-mail provider that is looking to improve their spam filter. The training data would consist of words from e-mails that have been classified as either “spam” or “not spam”. From there, the class conditional probabilities and the prior probabilities are calculated to yield the posterior probability. The Naïve Bayes classifier will operate by returning the class, which has the maximum posterior probability out of a group of classes (i.e. “spam” or “not spam”) for a given e-mail. This calculation is represented with the following formula:

![Formula to calculate maximum posterior probability](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/4e/2e/Naive_Bayes_Mathematical_Formula.png)

Since each class is referring to the same piece of text, we can actually eliminate the denominator from this equation, simplifying it to: 

![Simplified formula to calculate maximum posterior probability](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/77/95/Naive_Bayes_Simplified_Formula.png)

The accuracy of the learning algorithm based on the training dataset is then evaluated based on the performance of the test dataset.  

Class-conditional probabilities 

To unpack this a little more, we’ll go a level deeper to the individual parts, which comprise this formula. The class-conditional probabilities are the individual likelihoods of each word in an e-mail. These are calculated by determining the frequency of each word for each category—i.e. “spam” or “not spam”, which is also known as the maximum likelihood estimation (MLE). In this example, if we were examining if the phrase, “Dear Sir”, we’d just calculate how often those words occur within all spam and non-spam e-mails. This can be represented by the formula below, where y is “Dear Sir” and x is “spam”.

![Conditional probability formula for spam example](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/27/a7/Conditional_Probability_of_Spam_Example.png)

Prior probabilities

The prior probabilities are exactly what we described earlier with Bayes’ Theorem. Based on the training set, we can calculate the overall probability that an e-mail is “spam” or “not spam”. The prior probability for class label, “spam”, would be represented within the following formula: 

![Formula to calculate the probability of spam](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/b6/74/Probabily_of_Spam.png)

The prior probability acts as a “weight” to the class-conditional probability when the two values are multiplied together, yielding the individual posterior probabilities. From there, the maximum a posteriori (MAP) estimate is calculated to assign a class label of either spam or not spam. The final equation for the Naïve Bayesian equation can be represented in the following ways: 

![Naïve Bayesian equation](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/82/c4/Naive_Bayes_Mathematical_Formula_v2.png)

Alternatively, it can be represented in the log space as naïve bayes is commonly used in this form: 

![Alternative way to represent the Naïve Bayesian equation](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/e8/74/Naive_Bayes_Mathematical_Formula_LogForm.png)

Evaluating your Naïve Bayes classifier 

One way to evaluate your classifier is to plot a confusion matrix, which will plot the actual and predicted values within a matrix. Rows generally represent the actual values while columns represent the predicted values. Many guides will illustrate this figure as a 2 x 2 plot, such as the below:

![Visualization on how to interpret a confusion matrix](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/35/30/ConfusionMatrix.png)

However, if you were predicting images from zero through 9, you’d have a 10 x 10 plot. If you wanted to know the number of times that classifier “confused” images of 4s with 9s, you’d only need to check the 4th row and the 9th column.

![Confusion matrix example](https://www.ibm.com/content/dam/connectedassets-adobe-cms/worldwide-content/cdp/cf/ul/g/c0/c7/ConfusionMatrixExample.png)

Types of Naïve Bayes classifiers

There isn’t just one type of Naïve Bayes classifier. The most popular types differ based on the distributions of the feature values. Some of these include: 

- **Gaussian Naïve Bayes (GaussianNB)**: This is a variant of the Naïve Bayes classifier, which is used with Gaussian distributions—i.e. normal distributions—and continuous variables. This model is fitted by finding the mean and standard deviation of each class. 
- **Multinomial Naïve Bayes (MultinomialNB)**: This type of Naïve Bayes classifier assumes that the features are from multinomial distributions. This variant is useful when using discrete data, such as frequency counts, and it is typically applied within natural language processing use cases, like spam classification. 
- **Bernoulli Naïve Bayes (BernoulliNB)**: This is another variant of the Naïve Bayes classifier, which is used with Boolean variables—that is, variables with two values, such as True and False or 1 and 0. 

All of these can be implemented through the [Scikit Learn](https://scikit-learn.org/stable/modules/naive_bayes.html) (link resides outside ibm.com) Python library (also known as sklearn).

Advantages and disadvantages of the Naïve Bayes classifier

Advantages

- **Less complex**: Compared to other classifiers, Naïve Bayes is considered a simpler classifier since the parameters are easier to estimate. As a result, it’s one of the first algorithms learned within data science and machine learning courses.  
- **Scales well**: Compared to logistic regression, Naïve Bayes is considered a fast and efficient classifier that is fairly accurate when the conditional independence assumption holds. It also has low storage requirements. 
- **Can handle high-dimensional data**: Use cases, such document classification, can have a high number of dimensions, which can be difficult for other classifiers to manage. 

Disadvantages:   

- **Subject to Zero frequency**: Zero frequency occurs when a categorical variable does not exist within the training set. For example, imagine that we’re trying to find the maximum likelihood estimator for the word, “sir” given class “spam”, but the word, “sir” doesn’t exist in the training data. The probability in this case would zero, and since this classifier multiplies all the conditional probabilities together, this also means that posterior probability will be zero. To avoid this issue, laplace smoothing can be leveraged. 
- **Unrealistic core assumption**: While the conditional independence assumption overall performs well, the assumption does not always hold, leading to incorrect classifications. 

Applications of the Naïve Bayes classifier

Along with a number of other algorithms, Naïve Bayes belongs to a family of data mining algorithms which turn large volumes of data into useful information. Some applications of Naïve Bayes include:

- **Spam filtering**: Spam classification is one of the most popular applications of Naïve Bayes cited in literature. For a deeper read on this use case, check out this chapter from [**Oreilly**](https://www.oreilly.com/library/view/doing-data-science/9781449363871/ch04.html) (link resides outside ibm.com).  
- **Document classification**: Document and text classification go hand in hand. Another popular use case of Naïve Bayes is content classification. Imagine the content categories of a News media website. All the content categories can be classified under a topic taxonomy based on the each article on the site. Federick Mosteller and David Wallace are credited with the first application of Bayesian inference within their 1963 [**paper**](https://www.jstor.org/stable/2283270) (link resides outside ibm.com). 
- **Sentiment analysis**: While this is another form of text classification, sentiment analysis is commonly leveraged within marketing to better understand and quantify opinions and attitudes around specific products and brands. 
- **Mental state predictions**: Using fMRI data, naïve bayes has been leveraged to predict different cognitive states among humans. The goal of this [**research**](https://www.researchgate.net/publication/228714347_Machine_learning_of_fMRI_virtual_sensors_of_cognitive_states) (link resides outside ibm.com) was to assist in better understanding hidden cognitive states, particularly among brain injury patients.