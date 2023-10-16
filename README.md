# Project Title
Comparing Classifiers

## Description
This repo contains the CRISP-DM framework applied on Bank marketing data set from [UCI](https://archive.ics.uci.edu/dataset/222/bank+marketing)

* [Jupyter Notebook](https://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/comparing-classifiers-bank-marketing-dataset.ipynb)
    * Jupyter Notebook containing code used to perform this analysis and model development.
* [Readme](https://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/README.md)
    * Project description
* [Dataset](https://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/data/bank-additional-full.csv)
    * This dataset is from [UCI](https://archive.ics.uci.edu/dataset/222/bank+marketing).
* [CSISP-DM-BANK.pdf](hhttps://github.com/ddurgoji/comparing-classifiers-bank-marketing-dataset/blob/main/CRISP-DM-BANK.pdf)
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
* Random Forest Regression model had higher accuracy.
* Plotted a line graph to compare performance of all 4 models that were built.


#### Deployment
* Developed a Python function which accepts below inputs and provides price prediction using Random Forest Regression model.
  * Manufacturer
  * Model
  * Condition
  * Cylinders
  * Fuel
  * Title status
  * Transmission
  * Drive
  * Size
  * Type
  * Paint color </br>

Deployed the Model on Digital Ocean via Flask Server. Below sample API can be used to get used car price prediction.
```json
curl -H "content-type: application/json" http://164.90.154.175:8000/predict -X POST -d '{"year": 2022, "manufacturer": "tesla", "model": "model s", "condition": "good", "cylinders": "5 cylinders", "fuel": "electric", "odometer": 3996, "title_status": "clean", "transmission": "other", "drive": "4wd", "size": "full-size", "type": "sedan", "paint_color": "white" }'
```
Note: I will stop this server in a weeks time i.e on 09/05/2023.

#### Next Steps
* Continue to analyse each features further and play with it to improve model performance.
* Apply XGBoost and other algorightm once we go through it in future modules.


#### Recommendation to Car dealership
* Year, Odometer are most important items which consumers value most and determines price range of the car.
* Diesel and Electric can sell for higher prices when compared to gas car.
* Higher No of cylinders drive the car price up.
* Title status and condition affects the prices. Salvaged cars are penalized more and brings down prices.
* rwd are penalized more when compared to fwd/4wd. Rwd cars have lower price points.
* Automatic and other transmission type have higer price points and Manual reduces the car price.

These are some of recommendation which car dealership can use to procure used car to drive sales up and provide great customer satisfaction.
Complete details are in [Jupyter Notebook](https://github.com/ddurgoji/used-cars-price-prediction/blob/main/used-cars-price-prediction.ipynb).

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
