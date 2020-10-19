# Comparison supervised ML approches on CharityML Data
This notebook is based on a real existing dataset which is published by [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Census+Income). The dataset was donated by Ron Kohavi and Barry Becker, after being published in the article _"Scaling Up the Accuracy of Naive-Bayes Classifiers: A Decision-Tree Hybrid"_.

I used this notebook to discuss different supervised learning approaches. In the notebook you can find evaluations of a logistic regression, a K-Nearest-Neighboor, a Support Vector Machine, a Decision Tree and the ensemble methods Random Forest, AdaBoost and XGBoost Classifyer.

The whole notebook is commented and contains notes on my approach. I hope you enjoy the reading.

**Concluding remarks on the models:**
- Although the logistic regression was one of the faster models, the scores (Accuracy 0.85, F1 0.70) are not bad. It also shows that the method would be usable even with 10% of the sample size.
- As expected, the KNN has a longer training time (19.62) and is also subject to logistic regression in the results (Accuracy 0.82, F1 0.63). The sample size is similar to the logistic regression.
- The SVC has by far the longest training time (>1min), with the pred_time it is equal to the KNN. In addition, the results with (Accuracy 0.84, F1 0.67) are modest.
- The Desicion Tree clearly shows the problem of overfitting in training, even with fantastic values (Accuracy 0.97, F1 0.96), it worsens when tested for an Accuracy of 0.82 and an F1 of 0.63. Not surprisingly, but clearly the weakness of the method is evident here.
- The random forest has a short pred_time of 0.23. Moreover, the values of 0.84 accuracy and 0.68 F1 are good, but other models are better.
- The AdaBoost already had an accuracy of 0.86 and an F1 score of 0.72 in the baseline model, which put it just ahead of the random forest and was only exceeded by one model.
- The XGBoost had a long training time of 5.14 but also the best scores (Accuracy 0.87, F1 0.75).
