### Project Description:
This project includes a Python implementation of an MLP used to contrast gradient descent with stochastic gradient descent on two datasets. The first dataset is the "pumadyn32nm" dataset. This dataset is created using a robot arm simulator and contains 32 floating point features. The objective of the network when applied to this dataset is to estimate the angular acceleration of one of the robot arm links. The second dataset is called the "iris" flower dataset. This dataset contains just 4 floating point features and 3 classification categories pertaining to 3 different flower types. Both gradient descent and stochastic gradient descent were manually applied without the use of PyTorch to both datasets. The results are illustrated below.

### "pumadyn32nm" Dataset:
#### Gradient Descent:
The first 1000 training data points of the "pumadyn32nm" dataset were used. The following learning rates were tested: 0.1, 0.01, 0.001, 0.0001, 0.00001. The training error plots pertaining to each learning rate are illustrated in the Figures below:

From the Figures above, small learning rates did not allow the network to learn quick enough. Larger learning rates, however, caused rapid convergence. A considerably large learning rate of 0.1 did not cause oscillation or instability in the error plot evidenced by Figure _. A reason for this could be that the input and output data have a trivial correlation and a smooth feature space. 

#### Stochastic Gradient Descent:
For stochastic gradient descent, the following learning rates were used: 0.01, 0.001, 0.0001, 0.00001. Just as above, the error plots are illustrated below:

Oscillation and instability are present in every plot. From the results above, we can conclude the stability that comes from the nature of gradient descent was neccessary for the application of an MLP to the pumadyn32nm dataset.

### "iris" Dataset:
#### Gradient Descent:
Gradient descent was also applied to the "iris" dataset. The negative logarithmic likelihood plots for learning rates of 0.1, 0.01, 0.001, 0.0001, 0.00001 are delineated below:

Smooth training error plots are observed. As the learning rate increases, we see more rapid decreases in the negative log likelihood. When the leraning rate reached 0.1, howeover, oscillation and divergence occurs.

#### Stochastic Gradient Descent:
Similarly, for the same learning rates as above, the negative logarithmic likelihood was plotted for stochastic gradient descent. These results are shown below:

From the above, we can see that larger learning rates create more rapid convergence, but are prone to instability and oscillation. When compared to the gradient descent results, we can see that gradient descent produces more reliable results with a stronger global minimum. 


