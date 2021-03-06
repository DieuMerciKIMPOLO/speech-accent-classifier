# Speech Accent Classifier

Play around with the model and make predictions using the [web app](https://speech-accent-classifier.herokuapp.com/)
I made using Flask.

Read the [blog post](https://stephenjkaplan.github.io/2020/08/25/speech-accent-classifier/).

#### Description
Classifying audio of human speech into various accents/countries of origin using 
[MFCC coefficients](https://en.wikipedia.org/wiki/Mel-frequency_cepstrum) extracted from audio .wav files.

The model in `flask_app/static/sklearn_models/final_model.pkl` is an ensemble of K-Nearest Neighbor and Logistic 
Regression models. The overall predictive accuracy of the model is `0.89` and it has an ROC AUC score of `0.95`. The 
blog post about it is  [here](https://stephenjkaplan.github.io/2020/08/25/speech-accent-classifier/).

This was developed over a 2-week span in August 2020 as a project for the [Metis](https://thisismetis.com) data science 
program.

#### Data Source
Fokoue, E. (2020). [UCI Machine Learning Repository - Speaker Accent Recognition Data Set](https://archive.ics.uci.edu/ml/datasets/Speaker+Accent+Recognition). Irvine, CA: University of California, School of Information and Computer Science.

#### File Contents
* Running `main.py` will launch the Flask app locally.
* `utilities.py` contains files needed for the Flask app to run.
* `notebooks/` contains the Jupyter Notebook used to do all data analysis and modeling, as well as an accompanying 
   file of Python functions.
* `templates/` contains HTML files for the Flask application
* `static/` contains static files for the Flask application as well as the pickled scikit-learn model.
* `heroku.yml` and `Dockerfile` are used for deployment of the Flask app to Heroku

#### Dependencies

The contents of `/notebooks` can't be fully run because the Jupyter Notebook connects to a remote SQL database. In order 
to install the dependencies for the flask app, run:

`pip install -r requirements.txt`
