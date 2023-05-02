Download Link: https://assignmentchef.com/product/solved-cmu10403-homework2-imitation_learning
<br>
<h1>Problem 1: Behavior Cloning and DAGGER</h1>

In this problem, you will implement behavior cloning using supervised imitation learning from an expert policy. This problem and the GAIL one will be implemented in the following Colab notebook:

<a href="https://colab.research.google.com/drive/1dlur0hqm9hrGBflReCzNCwLBt5MnGtb5">https://colab.research.google.com/drive/1dlur0hqm9hrGBflReCzNCwLBt5MnGtb5</a>

This Colab notebook runs in the cloud, so you should not need to install anything on your laptop.

<h2>Background: Imitation Module</h2>

We have provided you with some function templates in the Colab notebook that you should implement. If you need to modify the function signatures, you may do so, but specify in your report what you changed and why.

<h2>Preliminaries</h2>

<strong>The following is the same as HW1’s CMA-ES question, you can copy your solutions from there.</strong>

First, you will implement a TensorFlow/Keras model. You will use this model a number of times in the subsequent problems. To test that your model is implemented correctly, you will use it to solve a toy classification task.

Next, you will implement a function to collect data using a policy in an environment.

This function will be used in subsequent problems.

<h2>Behavior Cloning</h2>

Start by implementing the train() method of the Imitation class. To test your behavior cloning implementation, you will run the following cell titled “Experiment: Student vs Expert.”

<ol>

 <li><strong>[15 pts] </strong>Run your behavior cloning implementation for 100 iterations. Plot the reward, training loss, and training accuracy throughout training.</li>

 <li><strong>[10pts] </strong>This question studies how the amount of expert data e↵ects the performance. You will run the same experiment as above, each time varying the number of expert episodes collected at each iteration. Use values of 1, 10, 50, and 100. As before, plot the reward, loss, and accuracy for each, remembering to label each line.</li>

</ol>

<h2>DAGGER</h2>

In the previous problem, you saw that when the cloned agent is in states far from normal expert demonstration states, it does a worse job of controlling the cart-pole than the expert. In this problem you will implement the DAGGER algorithm [2]. Implementing DAGGER is quite straightforward. First, implement the generate dagger data() method of the Imitation class. Second, in the cell titled “Experiment: Student vs Expert,” set mode = dagger.

<ol>

 <li>Run your DAGGER implementation for 100. Plot the reward, training loss, and training accuracy throughout training. We have included code for plotting in the following cell.</li>

 <li><strong> </strong>This question studies how the amount of expert data e↵ects performance. You will run the same experiment as above, each time varying the number of expert episodes collected at each iteration. Use values of 1, 10, 50, and 100. As before, plot the reward, loss, and accuracy for each, remembering to label each line.</li>

 <li>Does your DAGGER implementation outperform your behavior cloning implementation? Generate a hypothesis to explain this observation. What experiment could you run to test this hypothesis?</li>

</ol>