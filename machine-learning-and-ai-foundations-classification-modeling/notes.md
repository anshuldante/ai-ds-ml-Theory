# Classification modelling

## **Defining the Classification Strategy**

* ### Importance of Binary Classification

  * There are two famous myths regarding classification:
  * Each usecase = One best Algorithm, and if we define the problem properly, we'll kno which one to use. In general, this is a one-to-many relation between the problems and the solutions.
  * The goal of projects is one model. In real world usecases, we generally have multiple models sending info back and forth to make the final decision.
  * Binary classifiers play a role in all predictive analytics projects.

* ### Binary vs Multinomial: :dancers

  * The best part about binary classification is: there's a 50% chance of being correct to start with.
  * As we move into 3/4/5 categories the chances become 33%/25%/20%, even if we double the chances, 40% is still pretty bad.
  * Some valid usecases are: cluster-analysis
  * The model also gets very complicated if there are more than 2 categories.
  * If you do have a business usecase for more than 2 categories, try to still go down to 2.
  * Targets with more than 2 categories should be kept rare.

* ### Black-Box techniques

  * Neural networks
  * An ensemble of models: Random forest
  * To explain or to predict?
  * If the explanation is required, skip the black box techniques.
  * The older techniques persist because they are the best option.

* ### One task, many algorithms

  * Trial and error is the only way to find the best algorithm for a problem at hand.

* ### Statistics vs machine learning

  * Statistical algorithms are old and complex to understand, but they're still used:
    * Experts still use them
    * They are transparent in general
    * They are scalable
    * You can include both in an ensemble

* ### Model assessment vs business evaluation

  * Model assessment is ranking models on technical criterion.
  * Business evaluation looks at models performance based on ROI, performance indicators and management criteria.

----

## **Choosing a Winner**

* ### Training and test partitions

  * To start with, you break down the historical data into 2 partitions:
    * 50% for training
    * 50% for testing
  * As the dataset size gets smaller, the percentage for training data increases and test data decreases
  * There's an argument for a third partition, 50% training (candidate models), 25% test (candidate models), 25% validate (final model)
  * Another way to go about it is: use historical data only for training and test -> evaluate models using various technical approaches, and when the model is ready, run it on the data that has accumulated while you were building the model.
  * Some ways to evaluate models:
    * Lift Charts
    * Gains tables
    * Confusion matrix

----

## **Algorithms**

* ### Common issues

  * Interactions between variables: do the variables contribute to the model individually or they interact with each other?
  * Missing data handling
  * Over-fitting/under-fitting: not complex enough will lead to lower accuracy, too complex and it won't fix the new data well.
  * Feature selection: how does it determining which variables to use and how important those variables will be.

* ### Things to attend to

  * Does it use all or some of the variables?
  * Does it use all or some of the test data?
  * Situations where the model will perform well or bad.

* ### Discriminants (Linear Discriminant Analysis) with three categories

  * 

* ### Discriminants with two categories

* ### Stepwise discriminants

* ### Logistic regression

* ### Stepwise logistic regression

* ### Decision trees

* ### KNN

* ### Linear SVM

* ### Neural nets

* ### Bayesian networks

* ### Ensembles
