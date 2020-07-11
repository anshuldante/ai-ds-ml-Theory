# Machine Learning

* **Popular Algorithms:**
  * Decision Trees
  * **K-nearest neighbors (lazy learning):** find the k nearest neighbors.
  * **K-mean Clustering l(azy learning):** build k clusters of similar data.
  * **Regression**
    * **Linear:** based on past data, a predictor line is created and it's used to forecast future prospects.
  * **Naive Bayes:** cause it assumes that all predictors are independent of each other.
    * Assigns a probability value for a new dataset belonging to a class for all classes based on all predictors.
      * Ex. classifying dogs based on their hair, height and weight assuming that the 3 predictors are independent.
    * Sometimes a weighted predictor factor is used to give preference to one or more of the predictors.

* **Lazy Learning/Instance Based:** runs only when something has to be classified, take a lot of computation power and time.
* **Supervised**: classify data
* **Unsupervised**: cluster data

* **Bias**: gap between predicted value and actual outcome.
* **Variance**: when predicted values are scattered.

* **High bias and low variance**: consistently wrong in a consistent way.
* **High bias and high variance**: consistently wrong in an inconsistent way.

```python
    Eg.
    1. All 5 arrows hitting the centre: low bias and low Variance
    2. All 5 arrows landed close to the centre: low bias and high variance.
    3. All 4 arrows hitting one point in the outer circle: high bias and low variance.
    4. 2 hit the outer circle, 2 went behind and 1 fell below: high bias and high variance.
```

* **Under-fitting**: the model created using training-set is too simple and work well neither for training data nor unseen data.
* **Overfitting**: the model created using training-set fits the training dataset too much and doesn't work well for new data.

```python
Eg. a website that connects buyers with sellers.
  The predictors were:
    1. Square footage
    2. Location
    3. Number of bathrooms.
    4. Number of beds.
  The model had a high variance and even houses with the same predictor values had very different prices.
  So new predictors were added: *quality of view, modern appliances and walk-ability*.
  This made the model more flexible since there were more predictors to be considered now.
  Now we could have a very complex model which will be really hard to understand.
  And it may not work well with new data.
```

* **Signal** is something you can use to make accurate predictions.
* **Noise** is the natural variance in data which may not offer any insights.
* The goal is to **capture as much as possible of the signal and not get distracted by the noise.**

* **Making decisions:**
  * Labeled data: Supervised
  * Un-labeled data: Unsupervised
  * Lots of un-labeled data: k-means
  * lots of labeled data: kNN or decision trees
  * Or just try some algorithms and pick the one that worked the best.

* **Supervised:**
  * Try decision trees, k-nearest and naive bayes and pick the one with the best resutls.
  * Or can try ensemble modeling:
    * Make different ensembles of ML algorithms.
    * Bagging: create several different version of the same ML algorithm.
      * Decision Trees: make several different trees using different predictors
        and average out the results if the results are very inconsistent.
    * Boosting: Using several different ML algorithms to improve results.
      * For ex. Using k-means with decision trees: feed the tree results into k-means
        and let the machine look for groupings (semi-supervised).
    * Stacking: stack different algorithms on top of each other to improve results.

* **Challenges:**
  * Making sure that the people in the org can ask interesting questions.
  * Keeping training and testing data separate: mixing training data into testing data means giving the algorithm the right answers.
  * Time investment: not to invest too much time finding the right algorithm.
  * Don't be concerned about a high bias towards an algorithm, it might just make sense to you.