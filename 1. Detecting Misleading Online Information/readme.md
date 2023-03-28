## Detecting Misleading Online Information

In this project, I have implemented Naïve Bayes classifiers and TF-IDF vectorization to detect misleading online news with an achieved accuracy rate of 96%.

![image](https://user-images.githubusercontent.com/21034990/228343256-5e1322a9-681f-497c-9d25-21f03190f246.png)<br>
<i>(Kaggle Fake and real news dataset)</i>

#### Naïve Bayes classifiers
Naïve Bayes classifiers is classic, in the sense of using the most frequently used Bayes' theorem to compute the conditional probability of individual words given the occurence in individual classes.  During inference, we could multiply the probabilities of each individual word in the corpus, take the class with the highest probability to achieve the multinomial classification.

#### Count tokenizer  
From the above example, we can see that counting occurence of a unique word provide information.  Therefore, the most basic form of tokenizing a corpus is to count unique word occurence, and represent each corpus with a vector of word count.

Example:<br>
D1 = “The cat chased the mouse.”<br>
D2 = “The dog chased the cat.”<br>
W = [cat, chased, dog, mouse, the]<br>
V1 = [1, 1, 0, 1, 2]<br>
V2 = [1, 1, 1, 0, 2]<br>

<img width="771" alt="image" src="https://user-images.githubusercontent.com/21034990/228344795-9131e74c-dba2-4dad-ae49-5f295d5a7310.png">

#### TF-IDF vectorization
However, we can see a drawback from count tokenizer.  Auxiliary words could be reoccuring but not providing additional information.  TF-IDF addresses this problem by vectorizing a corpus corresponding to the probability of term frequency and inverse document frequency of each word.

![image](https://user-images.githubusercontent.com/21034990/228353402-257dc6d4-422d-4588-8bdb-f06f4ac5d1ff.png)

#### Performance Evaluation
1.  With logistic regression + TF-IDF, accuracy ~99%
2.  With Naive Bayes classifier + count tokenizer, accuracy ~96%
![image](https://user-images.githubusercontent.com/21034990/228355013-9ce150a9-d98a-4a3f-9f58-7bcc131950b5.png)
![image](https://user-images.githubusercontent.com/21034990/228354229-4208cac6-8c7e-4f77-b717-2b264222c7d7.png)
