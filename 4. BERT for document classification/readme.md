 ## Detecting Misleading Online Information

In this project, I have implemented BERT to detect misleading online news with an achieved accuracy rate of 100%.

<img src ="https://user-images.githubusercontent.com/21034990/229953675-f705a435-b895-4db5-9f77-e9ca185a0d73.png" width=400><img src ="https://user-images.githubusercontent.com/21034990/228343256-5e1322a9-681f-497c-9d25-21f03190f246.png" width=600>
<i>(Dataset: Kaggle Fake and real news dataset.  Image: Unesco)</i>

#### K Fold for locating learning rate for dataset
The dataset in this study is partitioned into 5 folds, with each fold consisting of a corresponding training and validation set. For each fold, the model is trained with 3 different learning rates, and the resulting F1 score is evaluated on the validation set. The best learning rate is then selected, and the model is finally trained on the entire dataset using this learning rate.

#### BERT  
BERT is based on the transformer architecture from where the encoder part is extracted, and designed with bi-directional self attention.  In this project, BERT base with 12 encoders is implemented as a classifier towards identifying news authenticity.

![image](https://user-images.githubusercontent.com/21034990/228353402-257dc6d4-422d-4588-8bdb-f06f4ac5d1ff.png)

#### Performance Evaluation

              precision    recall  f1-score   support

           0       1.00      1.00      1.00        50
           1       1.00      1.00      1.00        63

    accuracy                           1.00       113
   macro avg       1.00      1.00      1.00       113
weighted avg       1.00      1.00      1.00       113

