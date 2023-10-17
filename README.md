# Project Title
Comparing Classifiers - Bank marketing dataset

## Description
This repo contains the CRISP-DM framework applied on Bank marketing data set from [UCI](https://archive.ics.uci.edu/dataset/222/bank+marketing)

* [Jupyter Notebook](https://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/comparing-classifiers-bank-marketing-dataset.ipynb)
    * Jupyter Notebook containing code used to perform this analysis and model development.
* [Readme](https://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/README.md)
    * Project description
* [Dataset](https://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/data/bank-additional-full.csv)
    * This dataset is from [UCI](https://archive.ics.uci.edu/dataset/222/bank+marketing).
* [CSISP-DM-BANK.pdf](https://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/CRISP-DM-BANK.pdf)
    * Contains technical paper on Bank marketing data mining.

## Summary
#### Business Understanding
The data is related with direct marketing campaigns (phone calls) of a Portuguese banking institution. The classification goal is to predict if the client will subscribe a term deposit (variable y).

In this project, i am trying to build various classifier models which helps banks to determine if a customer accepts term deposit or not and improve their revenue and customer base.

#### Data Understanding
* Read CSV Dataset using Pandas.
* Using Plotly plotted various histograms to understand distribution of various columns.

#### Data Preparation
* Used one-hot encoding to convert all categorical features to numerical features
* Removed all features with unknown labels in it to avoid redundancy

#### Modelling
* Scaled numerical and Target feature columns.
* Created Train(70%) and Test(30%) dataset.
* Built below Classifier models with default parameters:
  * Baseline model using DummyClassifier - Accuracy=51.246%
  * Logistic Regression - Accuracy=73.504%
  * KNN Classifier - Accuracy=72.613%
  * Decision Trees - Accuracy=72.364%
  * SVM Classifier - Accuracy=73.824%
* Built below classifier models with hyper parameter tuning using Randomized SearchCV
  * KNN Classifier - Accuracy=73.748%
  * Decision Trees - Accuracy=78.445%


##### Accuracy Graph for all models with default parameters
![alt text](https://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/images/accuracy.png?raw=true)

##### Performance report for all models with default parameters
![alt text](https://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/images/base_perf.png?raw=true)

##### Performance report for Decision Trees and KNN Classifier model with Default and Hyper parameter tuning models compared
![alt text](https://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/images/perf_with_rscv.png?raw=true)


#### Evaluation
* Decision Tree Classifier model performed well with higher accuracy, precision, recall, AUC.
* Plotted Bar plot(See above) to compare performances.


#### Deployment
* Pending. I will try to deploy this model whenever i get some time.

#### Next Steps
* Model Tuning to imporve performance by more feature engineering and other techniques like RFE etc.
* Try using different classifier models like
  * Guassian Naive Bayes
  * Random Forest
  * XGBoost
  * Use data imputation methods to improve data quality etc.


#### Conclusion
##### Summary
In this practical application project, I created multiple machine learning classifier models that predicts likelyhood of clients who would subscribe to a bank's term deposit. The best model was Decision Tree classifier with optimized hyperparameters. This model's performance is 86.36%.

This model had a precision of 0.8734 divided by a prevalence of 0.50 gives us 1.74, which means that the machine learning model helps us 1.74  times better than randomly guessing. The model was able to catch 60% of customers that will subscribe to a term deposit.

Banks can focus on targeting customers with high consumer price index and euribor3m(3 month indicator for paying off loans) as they have high importance features for the model and business.

##### Reflection
* Decision Tree performed well with higher accuracy, precision, recall and AUC
* SVC and KNN performed well after Decision Tree.
* Removing features with unknown label didn't help much with improving the performance.
* RandomizedSearchCV helped finding the better performing Decision Tree by 5%
* I felt dataset is very biased towards no class and this makes it very difficult to find a better performing model
* I believe i have done a good job in this practical application assignment and tried my best to find a better performing model
* Modelling is an art and i am sure i will improve on it as i work more on it.
* Current model had 87% of precision so i believe this helps Bank in finding customer who can accept Term deposit with high quality

##### Improvements
* **Model Tuning to imporve performance by applying more feature engineering and other techniques like RFE etc.**
* Try using different classifier models like
    * Guassian Naive Bayes
    * Random Forest
    * XGBoost
    * Use data imputation methods to improve data quality etc.

Complete Analysis, Models and other details are in [Jupyter Notebook](https://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/comparing-classifiers-bank-marketing-dataset.ipynb).

## Technologies Used
Below are some of important technologies used in this project.
* [Python](https://www.python.org)
* [Jupyter Lab Notebook](https://jupyter.org)
* [Plotly](https://plotly.com)
* [Seaborn](http://seaborn.pydata.org)
* [Pandas](http://pandas.pydata.org)
* [Scikit-learn](https://scikit-learn.org/stable/)
and some more.


## Author
Dhiraj Durgoji (djdhiraj.8189@gmail.com)
