##Project Overview - Ship Detection - ImageKings

Project Goal:

Generate a bounding rectangle predicting ship locations using test data set.

Theory of operation:

Taking the ground truth data, convert from RLC encoded mask of the ships to a single bitmap that contains a bounding rectangle that surrounds all the RLC masks

Implementation:

We plan to train on pairs of color images and ground truth 1 bit images created as decribed above.

The challenge will be to determine which pre build AWS machine learning model will be used / and the corresponding hyperparameter optimization.

Challenges include working through the descrepencies between the descriptions in the Kaggle site and the csv representations.

Current Status:

Downloading data to Jupyter notebook via Kaggle API, increased disk quota to 100 GB
