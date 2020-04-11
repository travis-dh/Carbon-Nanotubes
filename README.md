# Carbon Nanotubes: An Application of Machine Learning to Atomic Coordinates

This repository contains a Jupyter Notebook with a multi-variate feedforward neural network model and a separate gradient-boosted regression tree designed to calculate the coordinates of a given atom $<u', v', w'>$ within a sample of carbon nanotubes given initial coordinates $<u, v, w>$ and chiral indices $n$ and $m$. These results are compared to the atomic coordinates calculated by Density Functional Theory, an extremely popular and accurate quantum mechanical modelling method used in the physical sciences. The neural network utilizes the Adam optimizer, a stochastic gradient-based optimizer. 

Note that this README.md containes a simple introduction and summary, both of which are also included in the Jupyter Notebook. For Data Scientists and others looking to verify findings or for more technical details, please refer to the contents of the Jupyter Notebook.

## Summary
Despite the accuracy of Density Functional Theory, the comparable accuracy and massive speed-up in computational time of the multi-variate gradient-boosted regression model and the sequential feedforward neural network leaves either of them a better option for calculating the coordinates of carbon atoms. 

Even though the gradient-boosted XGBRegressor performed slightly better than the neural network, the XGBRegressor depends on a `sklearn` wrapper for multi-variable support and a GridSearch for hyperparameter optimization which adds a few minutes to the approach. On the other hand, the performance of the neural network may be improved with, perhaps, a different optimizer, a different activation function, or maybe even an entirely different architecture. Further research can be done into optimizing a neural network for this task (the optimization of a neural network is an open problem in general) and/or expanding the original dataset by adding relevant features and parameters for model construction.

The dataset used in the Jupyter Notebook was downloaded from the [University of California, Irvine's Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Carbon+Nanotubes). A special thanks is to be given to the original authors Mehmet Acı and Mutlu Avcı, whose work is cited below.

Acı, M., Avcı, M. Artificial neural network approach for atomic coordinate prediction of carbon nanotubes. Appl. Phys. A 122, 631 (2016). https://doi.org/10.1007/s00339-016-0153-1
