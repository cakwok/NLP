## Detecting Misleading Online Information

In this project, I have implemented Naïve Bayes classifiers and TF-IDF vectorization to detect misleading online news with an achieved accuracy rate of 96%.

![image](https://user-images.githubusercontent.com/21034990/228343256-5e1322a9-681f-497c-9d25-21f03190f246.png)<br>
<i>(Kaggle Fake and real news dataset)</i>

#### Naïve Bayes classifiers
Naïve Bayes classifiers is classic, in the sense of using the most frequently used Bayes' theorem to compute the conditional probability of individual words given the occurence in individual classes.  During inference, we could multiply the probabilities of each individual word in the corpus, take the class with the highest probability to achieve the multinomial classification.

#### Count tokenizer  
From the above example, we can see that counting occurence of a unique word provide information.  Therefore, the most basic form of tokenization is to count unique word occurence, and represent each corpus with a vector of word count.

<img width="771" alt="image" src="https://user-images.githubusercontent.com/21034990/228344795-9131e74c-dba2-4dad-ae49-5f295d5a7310.png">
<i>(Real and fake news dictionary)</i>

<img width="345" alt="image" src="https://user-images.githubusercontent.com/21034990/228352227-a15fd7d0-a5f5-4831-9795-ade7e1d9c5a2.png">

#### TF-IDF vectorization
However, we can see a drawback from count tokenizer.  Auxiliary words could be reoccuring but not providing addtional information to the classifier.  TF-IDF addresses this problem by vectorizing a corpus corresponding to the probability of term frequency and inverse document frequency of each word.

![image](https://user-images.githubusercontent.com/21034990/228348643-6949c322-61e3-4ee5-b218-15e620505468.png)

Implemented the solution from scratch using Python, scikit-learn, Numpy, Pandas.

