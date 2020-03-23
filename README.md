# Flipr_Hackathon

This project is all about predicting the COVID-19 Infect_Prob in a person using the various different parameter avaliable in the dataset. The project is divided into 2 parts.

- Part-01: 
The objective of the first part of the problem statement is to predict the probability of a person getting infected by Covid-19 on 20th March 2020. The output file 01 should contain only people_ID and the respective infect_prob for the test data.

- Part-02:
The Diuresis of a person is a time-dependent parameter, for which you have to come up with a Time-series prediction model. Using the Diuresis predicted by the model, you need to calculate the infect_prob on 27th March 2020 for every people_ID in the test data. . The output file 02 should contain only people_ID and the respective infect_prob on 27th March. 

- For part 1, I have developed a model based on Support Vector Regression (SVR) which basically uses the Radial Based function i.e. rbf kernel
and using C and gamma as a parameter. Since to predict the better model based on kernels I split train and test the "Train Dataset.xlsx"
and used rbf and linear kernel.
The Mean Absolute Error, Squared Mean Error were better compare to rbf kernel.
![rbf](https://user-images.githubusercontent.com/37845653/77282374-bea9bd00-6cef-11ea-9cbb-3552c2e37033.JPG)
![linear](https://user-images.githubusercontent.com/37845653/77282376-bf425380-6cef-11ea-840c-a5ceda345cef.JPG)
![metric](https://user-images.githubusercontent.com/37845653/77282370-bc476300-6cef-11ea-823e-1380b6f7d162.JPG)

Since while predicting the Infect_prob of "Test dataset.xlsx" through training "Train dataset.xlsx" I used just rbf kernel along with C and gamma parameter taking the value randomly. I tried using linear kernel but it took lot of time to train due to time constraint I used rbf kernel. Even though I tried to get best model and parameter using Grid Search Optimization but it took lot of time and due to time 
constraint I just used rbf kernel to train the model and predict the Infect_Prob.  

- For part 2, I have made a Long Short Term Memory (LSTM)- Time series Prediction model to predict Infect_prob on 27th March. The idea behind the model is to predict the Diuresis value on 27th March and then predict the Infect_Prob. To predict the Diuresis value on 27th March I develop a LSTM model through window size i.e. Taking 4 window and predict the 5th window. Since in dataset sheet_name="Diuresis_TS" the diuresis value is from 20th March to 26th March so with the help of window size I predict the Diuresis value on 27th March.
   - After perdicting the diuresis value on 27th March, I substutited the value of diuresis of train dataset with diuresis value of 27the march. After doing this procedure I train the model using SVR as rbf kernel and fitted the model predicted the Infect_Prob of Test dataset. 
