# Flipr_Hackathon

This project is all about predicting the COVID-19 Infect_Prob in a person using the various different parameter avaliable in the dataset.
The project is divided into 2 parts
Part-01: 
The objective of the first part of the problem statement is to predict the probability of a person getting infected by Covid-19 on 20th March 2020. The output file 01 should contain only people_ID and the respective infect_prob for the test data.

Part-02:
The Diuresis of a person is a time-dependent parameter, for which you have to come up with a Time-series prediction model. Using the Diuresis predicted by the model, you need to calculate the infect_prob on 27th March 2020 for every people_ID in the test data. . The output file 02 should contain only people_ID and the respective infect_prob on 27th March. 

For part 1, I have developed a model based on Support Vector Regression which basically uses the Radial Based function i.e. rbf kernel
and using C and gamma as a parameter. Since to predict the better model based on kernels I split train and test the "Train Dataset.xlsx"
and used rbf and linear kernel.
The Mean Absolute Error, Squared Mean Error were better compare to rbf kernel.
