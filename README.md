# Flood-Prediction-Model

Train Dataset Link: https://www.kaggle.com/competitions/playground-series-s4e5/data?select=train.csv
Test Dataset Link: https://www.kaggle.com/competitions/playground-series-s4e5/data?select=test.csv

I have used a dataset that holds information about topographic drainage, emergency preparedness, urbanization, encroachments etc and these were used to predict flooding probability.
I first started off with checking for nulls or duplicates and since this dataset seemed pretty clean, I proceeded with splitting the dataset into training and validation sets. I then standardized the data by scaling the training set and then fit a Lasso Cross Validation model to identify the ideal lambda value.
After the best lambda value is identified, I fit a lasso model with the scaled training data along with best lambda value and predicted the flood probability for the validation data and used this model to predict the probability for the testing set.
I used R2 to assess the performance of the model and I observed that the model I constructed predicts flooding probability with 84.4% accuracy and has an MSE of 0.0004 which is really low.
