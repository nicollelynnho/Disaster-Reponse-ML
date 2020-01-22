# DisasterReponseML
Classify messages using a random forest model 

Summary:
This project is a message classifier. It classifies messages from a disaster into a variety of categories such as genre, aid_related or not, etc. Data was cleaned, loaded into a database, then modeled. Summary statistics are also visualized using a flask app.

Files in the repository:
- disaster_categories.csv is the raw data that shows what category the message falls into
- disaster_messages.csv is the raw data that shows the original and translated message
- process_data.py reads data from csv files, joins and cleans the data, then loads it into a sql database.
- train_classifier.py trains the data into a classifier model
- run.py runs the flask app. It controls the data visualizations and message classifier functionality on the web browser

### Instructions:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse`
    - To run ML pipeline that trains classifier and saves. Navigate to model file and run
        `python train_classifier.py sqlite:///../data/DisasterResponse.db model.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/
