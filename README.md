# fhir-patient-finder

This is a FHIR web application written in Python and using Flask as the backend.

Following are the FHIR server port numbers and the datasets hosted on that ports.

```
9090 -> synthea10 (demo dataset)
9091 -> synthea_ri_adult
9092 -> synthea_ri_peds
```

## 1. Dependencies
This app depends on Python 3 and a few Python packages outlined in the `requirements.txt` file. 

## 2. Before running the app

Change these parameters in the .env file. Use the port number assigned to you to run the app for FHIR_PORT.

```
FHIR_SERVER_BASE_URL= http://pwebmedcit.services.brown.edu:????/fhir
FHIR_USERNAME = ???
FHIR_PASSWORD = ???
FHIR_PORT=????
```

## 3. Running the App

We begin by creating a Python virtual environment using the `venv` module. This is done by running the command below from the "root" of this repo. 

```
python3 -m venv venv                 # create a virtual environment called venv

source venv/bin/activate             # activate our virtual environment

pip3 install -r requirements.txt     # install all our dependencies into the virtual environment
```


After the above steps, we should be able to launch our app using the following command.

```
python3 src/app.py
```


This will start the app on port "FHIR_PORT". You can open your preferred browser and see the app running on `http://localhost:FHIR_PORT` replace the FHIR_PORT with the actual port number assigned to you. 
The exact URL to the app can also be found on the terminal output after running the app.


