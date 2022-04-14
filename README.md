# Neural_Network_Charity_Analysis
## Overview
This project is a loan prediction risk analysis utilizing Tensorflow's Keras deep neural net learning model. Deep neural net learning models take an input of data points, reads the data processing for patterns, then passes these results to a new layer where it reads and processes again for deeper pattern recognition. This process can be repeated, within a reasonable process time, any number of times between any number of layers before it is given as an output to test for accuracy against the known target data in the initial dataset. In our case, the outcome is a sigmoid classification of success status on the return of loan made. The goal is to achieve 75%+ accuracy 
## Results
### Data Preprocessing
* The "IS_SUCCESSFUL" column in the initial data set denotes whether or not the loan is successfully returned on; this is considered our target for the Keras model.
* Borrower ask amount, borrower application type, borrower affiliation, borrower classification, borrower loan use and borrower organization are all considered features for predicting the target.
* Borrower EIN, borrower name, borrrower status, borrower special considerations and borrower income amount are dropped as features for predicting the target.
  * Borrower income amount included too many 0 entries
  * Borrower special considerations and borrower status included heavily lopsided value counts; the machine appeared to perform better without these features included
### Compiling, Training and Evaluating the Model
* Three neuron layers were used in the Keras model
  * Originally only two neuron layers were included, but adding a third improved model result
* The target model performance was not achieved.
  * The result achieved in the optimized notebook is 73.2% accuracy out of 75% goal.
* To increase the model's performance:
  * Adjusted number of layers
  * Adjusted number of neurons
  * Adjusted feature data selection; manage noisy data
  * Adjusted feature data preprocessing; manage noisy data
  * Adjusted layer activation functions
## Summary
Our goal of 75%+ target prediction was not achieved for this project. I believe that in order to reach this target, more changes need to be made to the front end data preprocessing and feature selection. Borrower ask amount could be bucketed to potentially resolve any issues with a great majority of these values belonging to $5000 and a few belonging to values magnitudes greater. Additionally, further analysis could be conducted up front to detemine how evenly split between loan return success some of these heavily sided features borower status are.
