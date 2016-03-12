# Airbnb New User Bookings
 
Predicting Airbnb user's first booking destination using Data Mining. 
Kaggle Competition : https://www.kaggle.com/c/airbnb-recruiting-new-user-bookings

### Installation Requirements : 
  
To run this project, you will need Jupyter - an interative iPython environment that runs in your web browser. The easiest way is to install Ananconda - https://www.continuum.io/downloads 

The notebooks use Seaborn in order to create charts. See https://stanford.edu/~mwaskom/software/seaborn/installing.html to install this library

In order to run the XGBoost notebook, the XGBoost library needs to be installed. See https://github.com/dmlc/xgboost/tree/master/python-package for installation instructions

### Data Folder : 

This contains the data files train_users_2.csv and test_users.csv. This project also requires sessions.csv which can be obtained from the kaggle competition site : https://www.kaggle.com/c/airbnb-recruiting-new-user-bookings/data
(Couldn't upload the sessions data file in the git as the size of the file is large)


#### Models_1 : 

This folder contains two iPython notebooks Preprocessing+Modeling and GradientBoosting_Analysis. 
Each notebook contains comprehensive steps to preprocess the data and run the models individually. The notebooks require train_users2.csv and sessions.csv to be in the same folder as the notebooks. 

Preprocessing+Modeling : This notebook has analysis on Linear Discriminant Analysis, Quadratic Discriminant Analysis, Gaussian Naive Bayes, AdaBoost and Gradient Boosting Classifiers.

GradientBoosting_Analysis : This notebook focuses on the Gradient Boosting Classifier.


#### Models_2 :

This folder contains 3 iPython notebooks. The notebooks require that train_user2.csv, test_users.csv, and sessions.csv be in the same folder.

Run Preprocessing.ipynb in order to prepare the data. Running this file creates the intermediate files which will be used by the other two notebooks.

logisticreg+ada.ipynb contains the various models for logistic regression, and AdaBoost with logistic regression.
xgboost_qda.ipynb contains the results of XGBoost and Quadratic Discriminant Analysis

#### Models_3 : 

This folder contains the iPython notebooks to model using Decision Tree and Random Forest. 
The Preprocess.ipynb contains the preprocessing file which requires the train_users_2.csv and test_users.csv to be in the same folder as the notebook. This will produce an output preprocessed_airbnb_train.csv and preprocessed_airbnb_test.csv .

The DecisionTree.ipynb notebook has the DecisionTree models. The RandomForest.ipynb notebook has the RandomForest models. To run this notebook, preprocessed_airbnb_train.csv has to be there in the same folder as the notebooks. A copy of the generated preprocessed_airbnb_train.csv is already available in the Models_3 folder.

The Experiments.ipynb notebook contains some experiments like binary classification, three class classification and some interesting findings observed while building those models.This also requires the preprocessed_airbnb_train.csv to be in the same folder as the notebook.


#### Ensemble Voting Classifier

The notebook VotingEnsemble.ipynb contains the voting classifier which uses the models LDA, Logistic regression and Decision Trees. To run this, the data file Models_3/preprocessed_airbnb_train.csv has to be in the same folder as the notebook.
