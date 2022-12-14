# DSCI510_final_project
# -------------------------------------

# Dependencies

> I have a `requirements.txt` file which contains all my dependencies and their version number.
I will list them here as well:
1. pandas==1.3.5
2. seaborn==0.11.2
3. numpy==1.21.5
4. matplotlib==3.5.2
5. scikit-learn==1.0.2
6. xgboost==1.6.2
7. requests==2.28.1
8. beautifulsoup4==4.11.1
9. fake-useragent==1.1.1
10. plotly==5.9.0
11. session-info==1.0.0

# Installation

How to install the requirements necessary to run your project:  

```
pip install -r requirements.txt
```
# Running the project

My project could be run by simply running the Jupyter Notebook file 

```
Final_Code.ipynb
```
It could be run using Cell->Run All

 How to re-produce my results:
- My code is a Jupyter Notebook (.ipynb) and it could be run using Cell->Run 
All
- One Potential Problem: CODE MAY TAKE HOURS TO RUN DUE TO WEBSCRAPING.
- The Analysis portion of the Code is not time consuming only the web scraping portion 
- To combat this problem of time, I recommend reading into pandas the (2022.csv) file
right before the heading in my Jupyter Notebook “DATA ANALYSIS AND 
PREPROCESSING”.
- I also explain this in my Jupyter Notebook. Reading in that CSV file should 
allow you to execute my Analysis and visualization Cells for that CSV.
- You will also need to read into pandas the (‘2023.csv’) file right before the
heading in my Jupyter Notebook “Read ('2023.csv') INTO PANDAS 
HERE”
- Reading into pandas ('2023.csv') will allow you to execute the remaining analysis and visualizations
- ALSO SET THE CORRECT VARIABLE NAMES FOR EXAMPLE:
```
data = pd.read_csv(r"2022.csv")
data2 = pd.read_csv(r"2023.csv")
```
# Methodology/Analysis

> What kind of analyses or visualizations did you do? (Similar to Homework 2 Q3, but now you should answer based on your progress, rather than just your plan)  

- My primary analysis was to build models that make predictions of the 
Fantasy Points and compare these models using specific scoring metrics I 
explained above to determine which model is the best for predictions.
- I found that the Linear Regression model is a perfect fit for the data,
making 100% accurate predictions. This makes perfect sense of course 
because I used as predictors the statistics of the players and the response 
(Fantasy Points) are a clear linear combination of the player statistics.
- My initial Regression Assumption was: “Expected values of Fantasy 
Points follow a regression function”. This was the basis to using 
Regression Models.
- The Best Model: Closest Model to the Regression Function 
- Therefore, Linear Regression was the best model it’s the closest to the 
regression function in fact it is the regression function. It also had the 
lowest MSPE and highest R^2 Score.
- When I made predictions on unseen new data (2022-2023 NBA Season), 
the results were very similar nearly identical.
- The Worst Model: KNN 
- KNN had the highest MSPE and the lowest R^2 score. The main 
difference between Linear Regression and KNN is that Linear Regression 
is a parametric model and KNN is a non-parametric model.
- Future Work: If given more time I would try making the relationship 
between predictors and response less linear by adding more predictors 
maybe even categorical predictors such as opponent defense rating etc.

# Visualization
- I made quite a few different types of visualizations.
- I plotted the distributions of the features and response (Fantasy PTS). 
- I also have visualizations of the predicted fantasy points vs actual fantasy 
points as scatter plots with an OLS trendline for each model.
- I have visualizations of the Top Features for some of my models and how 
important they were in making the predictions.
- I have visualizations of 3 players Actual Fantasy Points vs Predicted 
Models for the 2022-2023 NBA Season. Players: Nikola Jokic, Stephen 
Curry, Luka Doncic
- I used matplotlib, plotly, and seaborn libraries to create these visualizations
- ***INSIGHTS:*** 
  1. Some of these visualizations clearly show the best and worst model for prediction due to scatterplots
  2. Some of the Visualizations show the top features for that particular model. The top features of the model are the ones that are most important to the model when making predictions
  3. The Best Model is the closest model to the regression function. My visualizations show that indeed the true regression function is a Linear Regression as it fits the data perfectly and makes 100% accurate predictions with R^2 score = 1.0 and MSPE = 0 

# Future Work

> Given more time, what is the direction that you would want to take this project in?

 If given more time I would certainly incorporate more predictors in training my 
models. More categorical predictors like I said above Defense, Defense by 
position, home court advantage, etc. These would decrease the linear relationship between the predictors and the response variable (Fantasy Points) and therefore  may lead to a different Best Model.


