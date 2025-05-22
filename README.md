# End-to-End-Kidney-Diesease-Classification-Project

## How to run?
### STEPS:

Clone the repository

```bash
https://github.com/sudhanvabharadwaj/End-to-End-Kidney-Diesease-Classification-Project
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n kidney-cnn python=3.9 -y
```

```bash
conda activate kidney-cnn
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```

```bash
# Finally run the following command
python app.py
```

Now,
```bash
Open up your local host and port
```

## MLflow

- [Documentation](https://mlflow.org/docs/latest/index.html)

- [MLflow tutorial](https://youtu.be/qdcHHrsXA48?si=bD5vDS60akNphkem)

##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)

MLFLOW_TRACKING_URI=[your_tracking_uri] \
MLFLOW_TRACKING_USERNAME=[your_username] \
MLFLOW_TRACKING_PASSWORD=[your_password] \
python script.py

Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI = <your_tracking_uri>

export MLFLOW_TRACKING_USERNAME = <your_username> 

export MLFLOW_TRACKING_PASSWORD = <your_password>

```

## DVC cmd

1. ``` dvc init ```
2. ``` dvc repro ```
3. ``` dvc dag ```