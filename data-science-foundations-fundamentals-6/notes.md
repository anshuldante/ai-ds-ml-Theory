# Data Science Foundations

* **The pathway of Data-Science Projects:**
  * Planning
    1. Define goals
    2. Organise resources
    3. Coordinate people.
    4. Schedule Project.
  * Wrangling/prepping the data
    1. Get data
    2. Clean data
    3. Explore data
    4. Refine data
  * Modeling
    1. Create model
    2. Validate model
    3. Evaluate model
    4. Refine model
  * Applying
    1. Present model
    2. Deploy model
    3. Revisit model
    4. Archive assets

* **The Roles in a data science team:**
  * Engineer
    * Developers and architects
    * Focus on hardware and software that make data science possible
  * Machine Learning Specialist:
    * Extensive work in CS and maths
    * Deep Learning
    * Artificial Learning
  * Researcher
    * Focus on domain specific research
    * Physics/genetics, medicine, psychology
    * Statistical expertise
  * Analyst
    * Data-to-data tasks
    * Web Analytics, SQL, visualisations.
    * Good for business decision making
  * Manager
    * Manage data science projects
    * Frame business relevant questions and answers
    * Must "Speak data"
  * Entrepreneur
    * Data-based startups
    * Often need all skills including business
    * Creativity in planning and execution
  * The "UNICORN"
    * Also known as a ROCKSTAR or NINJA
    * The full stack data scientist who can do it all
    * Very rare

* **How Humans learn:**
  * Memorisation is hard
  * Spotting patterns is easy.
  * React well to new situations.
* **How Machines Learn:**
  * Memorisation is easy.
  * Spotting patterns is hard
  * New situations are challenging.

* **Teach/Train machines:**
  * Show the algorithm millions of labeled examples
  * The algorithm then finds its own distinctive features
  * The algorithm may not be relevant or visible to humans.

* **Neural Networks**
  * The theory has existed for years.
  * The required computing power has caught up
  * The data availability has caught up, primarily due to social media

* **Data Science without ML:**
  * Any traditional classification task: Decision trees, kNN, k-mean
  * Predictive models
  * Sentiment analysis

* **ML without data Science:**
  * Can be done without domain expertise
  * Better when used in collaboration.

* **Neural Networks:**
  * Tiny steps with data leading to amazing analytical results

* **Prescriptive Analysis:**
  * RCT: randomised controlled trial
  * Theoretically simple
  * Practically complex in general
  * A/B testing for web-design is rather simple.

* **Good clean data characteristics:**
  * Column=variable
  * Row=case
  * One sheet per file
  * One level of observation

* **Untidy Spread sheet:**
  * Titles
  * Images and figures
  * Colours as data
  * Merged cells
  * Sub-tables
  * Summary values
  * Comments and notes

* **Further problems with somewhat clean data:**
  * Meaning of Values and variables
  * Missing values
  * Misspelled text
  * Numbers as text
  * Outliers
  * Sample Info

* **Some more challenging input data mediums:**
  * Print PDFs
  * Print tables
  * Print Graphs
  * Emojis have 10 different ways of representation.

* **Apps for data analysis:**
  * JASP
  * SPSS
  * jamovi

* **Python:**
  * Currently the most popular language for Data Science and Machine Learning
  * General purpose language
  * Easy to learn

* **R:**
  * Specifically developed for Data Analysis
  * Popular with scientists and researchers.

* *Tensorflow*

* **MLaaS: Machine Learning as a Service**
  * Microsoft Azure ML
  * Amazon Machine Learning
  * Google AutoML
  * IBM Watson Analytics

* **MLaaS Advantages:**
  * Put analysis where the data is stored
  * Flexible Computing Requirements.
  * Drag and Drop Interface

* **Baye's Theorem:**
  posterior probability = probability of data given the hypothesis * prior probability / probability of the data found

* **Regression Analysis Pros:**
  * Flexible Data
  * Flexible models
  * Easy to interpret.

* **Trend Analysis:**
  * Plot a graph
  * Find a Function against time
    * Linear
    * Exponential
    * Logarithmic
    * Sigmoid
    * Sinusoidal
  * Change Points
    * Look for changes in the resting state of the Data
    * Then check for historical events to explain the changes.
  * Decomposition
    * Take trend over time and break it down into several elements.
    * Overall Trend
    * Seasonal/cyclic trend
    * Random/Noise

* **Clustering:**
  * KNN
    * Plot the data in a K-dimensional space
    * Measure the distances between different points.
  * K-Means
  * Density models
  * Distribution models.
  * Linkage clustering models.

* **Classifying:**
  * How TO:
    * Locate case in k-dimensional space.
    * Compare labels to nearby data Points
    * Assign the new case to a category
  * Algorithms:
    * K-Means: assign case to the closest of k centroids.
    * KNN: use the most common category of the k closest neighbours of the new case.
  * Types:
    * Binary: yes/no
    * Multiple categories: pics, emails etc.
    * Distance measures: euclidian distance etc.
    * Compare it to one or more central or centriod Points
    * Confidence level
  * Correctness of the algo:
    * Total accuracy: generic accuracy, may not always work too well
    * Sensitivity: the true positivity test: if some data is supposed to be in a category, what's the likely-hood of it getting classified in the correct category.
    * Specificity: true negative tests: Cases should only be categorised if they actually belong.

* **Baye's Theorem:** combine data based on Sensitivity, Specificity and base rates.

* **Anomalies:**
  * Fraud detection
  * Process failure
  * Potential value

* **Outliers:**
  * Cases that are distant from others.
  * Cases that don't follow an expected pattern.
  * Cases that match known anomalies.

* **Algorithms to detect anomalies:**
  * Regression
  * Bayesian analysis
  * Hierarchical clustering
  * Neural networks

* **Properties of anomalies**
  * Rare events: frauds are uncommon which lead to unbalanced models
  * Difficult data: biometrics, multimedia, time-Sensitive signatures.

* **Dimensionality reduction: used in a earlier phase to get the data ready.**
  * Reduce the number of variables and data
  * Try to use a single score to make decisions.
  * When you combine many variables and features, the errors seem to cancel out in general
  * Reduces the collinearity.
  * Improves speed
  * Improves generalizability
  * Principle component analysis (PCA): take multiple correlated variables and combine then into a single score/component
  * Factor analysis: find the underlying common factor which gives rise to individual components.

* **Feature selection and creation: used after dimension selection and to find the best features to look at.**
  * Deciding the greatest decision value for a feature:
    * Correlation with the outcome: and the ones with bigger correlation have a higher decision value, one variable at a time so can take time and is linear.
    * Step-wise regression: put the data points into a computer and let the computer find the decision value: generally considered a bad choice, since variation in data can have huge impact.
    * LASSO and Ridge regression:: least absolute shrinkage and selection: more modern ways of regression that better handle flukes of chance variation, give better score for variables' role in the equation and emphasis
    * Variable importance: for neural networks.

* **Things to keep in mind while selecting variables:**
  * Is it something we can control?
  * ROI of the variable: cost vs value
  * Is it sensible, does it make sense to be looking at this variable?

* **Validating models:**
  * Always check your work.
  * Build using training data -> cross-validate using internal testing data -> holdout testing data: 20% of untouched data. This should give you the true test of your model.

* **Aggression models:**
  * Combine the results of several different models.
  * Take the most common category from the models.
  * Average prediction in case of quantitative things.
  * Benefits:
    * Multiple perspectives
    * Find signal and Noise
    * More stable estimates
    * More generalizable results.

* *Interpretability is critical!*

* **Actionable insights!**
  * Focus on controllable things.
  * Think practically: ROI
  * Build up: improve over time.
