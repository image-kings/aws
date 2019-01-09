##Project Overview - Ship Detection - ImageKings

[APH] 1/9/2019 See latest update below...

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

>>> Update 1/9/2019

Using Sagemaker Semantic Segmentation (ignore above content)

Create 4 directories in S3 (that align with the segmenation example code along these lines):

1. Training JPEGs - contains training jpgs as input

2. Training Annotations - PNGs created from RLC training ship mask data, (ground truth) pixel index values of 1 = ship, values of 0 = notship (need to write python to do this for entries in train_ship_segmentation.csv)

3. Validation JPEGs - contains validation jpgs as input

4. Validation annotations - PNGs created from RLC validation ship mask data (ground truth), pixel inded values of 1 = ship, values of 0 = notship

Move data into S3

Setup instance for training

Train

Check results

Tune hyperparameters



