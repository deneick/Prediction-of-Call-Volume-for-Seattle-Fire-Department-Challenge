# Prediction of Call Volume for Seattle Fire Department

Dispatching emergency calls in a city is challenging: There are large variations over a year, saison
and especially time of day. Someone has to decide how many dispatchers are on duty for every day.
Hence, we are looking for a model, which can predict the call volume for each day of the year and
each hour of the day. 

We use the dataset from [data.seattle.gov](https://data.seattle.gov/Public-Safety/Seattle-Real-Time-Fire-911-Calls/kzjm-xkqj).

This repository contains a notebook, that will create scripts. 


## Setup and requirements

```python
pyenv local 3.9.8
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

After running the notebook, the scripts are used as follows:

```python
# Train and save a model
python train.py
# Predict and save results (First parameter is the Date including the hour. Second parameter is how many days you want to forecast.)
python predict.py 01-10-2022:16 7

# Train and test a model
python test.py
```