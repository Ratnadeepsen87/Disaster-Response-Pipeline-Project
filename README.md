# Disaster-Response-Pipeline-Project
This Project is part of Data Science Program - Disaster Response Pipeline Project.

## Project motivation
This Project is part of Data Science Nanodegree Program by Udacity in collaboration with Figure Eight. The aim of the project is to build a Natural Language Processing tool that categorizes messages using a prelabelled set.

As input, we have the real messages that were sent during disaster events. This has been provided by [Figure Eight](https://appen.com). Goal of this project is to build a classification model to categorize the messages so that they can then be sent to appropriate disaster relief agencies. 

The final project is a webapp that incorporates the classification model. In the webapp a user can input a message and get classification results in several categories.

The project consist of the following parts:
1. ETL Pipeline to clean, normalize, tokenize and lemmatize the data
2. Machine Learning Pipeline to build and train a model to categorize messages in the set categories
3. Web App to show a summary of the results as well as a tool to categoirze messages in real time

## Files

* data - containing:
  * 2 input files disaster_categories.csv and disaster_messages.csv
  * A database to store the cleaned data set DisasterResponse.db
  * ETL Pipeline process_data.py
  
* models - containing:
  * Machine Learning Pipeline train_classifier.py 

* app - containing:
  * Script to launch the Flask web app
  * templates folder with the html for the web app
  
## Pre-requisites
```
python3
pandas
sklearn
numpy
flask
plotly
sqlalchemy
nltk
```
## Installing

To clone the git repository:

```git clone https://github.com/Ratnadeepsen87/Disaster-Response-Pipeline-Project.git```

## Executing Program:
You can run the following commands in the project's directory to set up the database, train model and save the model.

1. To run ETL pipeline to clean data and store the processed data in the database ```python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/disaster_response_db.```

2. To run the ML pipeline that loads data from DB, trains classifier and saves the classifier as a pickle file ```python models/train_classifier.py data/disaster_response_db.db models/classifier.pkl```

3. Run the following command in the app's directory to run your web app. ```python run.py```

4. Go to http://0.0.0.0:3001/

# Acknowledgements
[Figure Eight](https://appen.com/) for providing the relevant dataset to build and train the model
