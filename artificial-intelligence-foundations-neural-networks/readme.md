# Neural Networks

* **Neural Networks, things to consider:**
  * Massive amounts of data required.
  * Empirical approach: need to run small experiments to get better results, the variables here are the network's hyper-parameters.

* **Perceptrons:**
  * It takes several binary inputs and produces a binary output.
  * Eg.

      ```python
      v1
      a. x1= Cleanliness = 1
      b. x2 = Spanish menu = 1
      c. x3 = Sombrero = 0

      v2
      a. x1= Cleanliness = 1 * 3
      b. x2 = Spanish menu = 1 * 6
      c. x3 = Sombrero = 0 * -3
      ```

* **Neurons:**

    ```python
    x1= Cleanliness = 0.9 * 3 = 2.7
    x2 = Spanish menu = 0.3 * 6 = 1.8
    x3 = Sombrero = 0.9 * -3 = - 2.7
    ```

  * Apply a sigmoid function let's say it gives 0.4
  * We add bias in a neuron to let it decide whether it need to fire or not. *Eg. Add bias = 1.8 + 5.*

  * The number for each neuron in the hidden layer is called the neuron's level of activation.
  * The network can almost be thought of as lighting up, as each of the input is passed through it.
  * Each neuron in a layer connects with all of the neuron in the next layer.
  * Like we'd ignore the background while searching for the dog's nose, neural networks do it using weights between connections.

* Cost of a correct result is the average of the sum of all other incorrect results.
* You want the cost to go down over time.
* Back-propagation can be used by the network to adjust the weights.
* While tuning, even 1 change in a high weighted neuron can change the results/cost drastically.
* In general, high weighted neurons stay in a cluster.
* Changing the weight of a level 1 neuron will have a big effect because of chaining.
