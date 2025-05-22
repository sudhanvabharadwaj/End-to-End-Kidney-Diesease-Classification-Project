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

## AWS-CICD-Deployment-with-Github-Actions

### 1. Login to AWS console.

### 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
### 3. Create ECR repo to store/save docker image
    - Save the URI: 905418092965.dkr.ecr.eu-north-1.amazonaws.com/kidney

	
### 4. Create EC2 machine (Ubuntu) 

### 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
### 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


### 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = <aws_region_name>

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = <app_name>
