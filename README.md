
![](https://github.com/Linchen106/Projekt-2/blob/main/Schwein_ks.jpg)


# Crowdfunding with kickstarter

Kickstarter is a US based global crowdfunding platform focused on bringing funding to creative projects. 
Since the platform’s launch in 2009, the site has hosted over [189.131](https://www.kickstarter.com/help/stats?lang=de) successfully funded projects with over 5.316.550.434 $ and 18.623.561 million unique backers. 
Kickstarter uses an “all-or-nothing” funding system. This means that funds are only dispersed for projects that meet the original funding goal set by the creator.

Unfortunately, not every campaign comes out as a winner. 

This is an exploratory data analysis of the kickstarter projects dataset for predicting if a kickstarter project is going to be successful or not.

### Data & SetUp
The dataset for this project was given by our head coaches. 
55 csv files were loaded and combined into a single data frame using the pd.read_csv function in python. 
The raw dataset could be found here. 

### Get a feeling for my data & business understanding
First of all we startedt to develope a rare understanding for the data & business case. 
For example we checked the shape, null values und the columns. 
To get an better feeling, we took our time to check each column and tried to figure out the meaning. 
After that we started with the online research to get some background information about kickstarter. 

### Data Preparation & Exploration
In the second step it took quiet a while to explore all our features and our target variable (state: successful or failed). 
In this [this notebook](https://github.com/Linchen106/Projekt-2/blob/main/EDA.ipynb)  you can find everything in detail. 

### Modelling & Hyperparameter Optimization
Before we started with different models a feature selection was performed to select the predictors which play a significant role in explaining if a project is going to be successful or not. In this [this notebook](https://github.com/Linchen106/Projekt-2/blob/main/BaseModel.ipynb)  you can find two different models (logistic regression and random forest) as our basismodel. The results of our basemodel can be regarded as a upper limit for the following analysis due to data leaking reasons. In our final mdoel we skip the features usd_pledged_amount and backers_count. The feature staff_pick can not be used for prediction as well. It is not clear if a project will be picked when it is launched.

In this notebook you can find different models ([AdaBoost](https://github.com/Linchen106/Projekt-2/blob/main/MainModel_AdaBoost.ipynb), [XGBoost](https://github.com/Linchen106/Projekt-2/blob/main/MainModel_XGBoost.ipynb), [Random Forest](https://github.com/Linchen106/Projekt-2/blob/main/MainModel_RanFor.ipynb) and [SVM](https://github.com/Linchen106/Projekt-2/blob/main/MainModel_SVM.ipynb)). For each method, we tweaked the value of parameters to get the best set out of it.

Alright...let's dive in!

