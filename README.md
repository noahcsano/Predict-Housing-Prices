# Predict-Housing-Prices

UC Berkeley Data 100 - "Principles and Techniques of Data Science" Project

Language: Python
Softwares, Libraries: Pandas, Numpy, Seaborn, Matplolib, Scikit-learn, Jupyter Notebook

The dataset we worked with for this project consists of over 500,000 records from Cook County, Illinois, the county where Chicago is located. The dataset has 61 features in total; the 62nd is sales price, which the model predicts with linear regression.

The data are split into training and test sets with 204,792 and 68,264 observations. The training set will be split into two groups: 80% train and 20% validation.

I first performed Exploratory Data Analysis, Feature Engineering, and seaborn/matplotlib visualizations to draw out the relationship between the provided features.(Ex: scatterplot, KDE Plot, jointplot, violinplot, etc.) Some variables required a log transformation of data in order to build a linear relationship with sales price. 

After choosing my features to train the model, I set up a sklearn.linear_model.LinearRegression model. 
I then fit the linear regression model and used it to compute the fitted values of Log Sale Price over the training data, and the predicted values of Log Sale Price for the validation data. I trained two separate modles with different features to compare the performance.

In order to measure the performance of the two models, I used root mean square to calculate the training error and validation error for both models. Since our model predicts Log Sale Price, I compute RMSE between the predicted and observed Log Sale Price.

Comparing the actual parameters (𝜃0 and  𝜃1) from both of our models.
For the 1st model : Log Sale Price = 𝜃0 + 𝜃1 ⋅ (Bedrooms)
For the 2nd model, Log Sale Price = 𝜃0 + 𝜃1 ⋅ (Bedrooms) + 𝜃2 ⋅ (Log Building Square Feet)
We found that the 2nd model 𝜃1 changes from positive to negative with the additional feature. 

As an addition to this project, we also created another model with arbitrary numbers of features and transformations in order to find the lowest RMSE scoring model. 
