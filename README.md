# Kidney Tumor and Stone Classification-MLflow-DVC
![alt text](https://github.com/sadhiin/kidney-disease-classification-DL-MLOPS/blob/main/media/dataset-cover.png)
## Introduction
Kidney Disease Classification is a project utilizing deep learning techniques to classify Kidney Tumor and Stone diseases from [medical images dataset](https://www.kaggle.com/datasets/nazmul0087/ct-kidney-dataset-normal-cyst-tumor-and-stone/). This project leverages the power of Deep Learning, Machine Learning Operations (MLOps) practices, Data Version Control (DVC), and integrates with DagsHub for collaboration and versioning.

## Project Overview
The main goal of this project is to develop a reliable and efficient deep learning model that can accurately classify kidney Tumor and Stone from medical images. This could include, but is not limited to, identifying different stages of cancer, detecting anomalies in X-rays, or diagnosing skin diseases through dermatological imaging.

## Importance of the Project
- **Enhancing Healthcare**: By providing accurate and quick disease classification, this project aims to significantly improve patient care and diagnostic accuracy.
- **Research and Development**: It serves as a tool for researchers to analyze medical images more effectively, paving the way for new discoveries in the medical field.
- **Educational Value**: This project can be used as a learning platform for students and professionals interested in deep learning and medical image analysis.

## Technical Overview
- **Deep Learning Frameworks**: Utilizes popular frameworks like TensorFlow or PyTorch for building and training the classification models.
- **Data Version Control (DVC)**: Manages and versions large datasets and machine learning models, ensuring reproducibility and streamlined data pipelines.
- **Git Integration**: For source code management and version control, making the project easily maintainable and scalable.
- **MLOps Practices**: Incorporates best practices in machine learning operations to automate workflows, from data preparation to model deployment.
- **DagsHub Integration**: Facilitates collaboration, data and model versioning, experiment tracking, and more in a user-friendly platform.

## Workflows

1. Update config.yaml
2. Update secrets.yaml [Optional]
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the dvc.yaml
10. app.py

# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/GauravSahu13/kidneyTumorClassification
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n cnncls python=3.8 -y
```

```bash
conda activate cnncls
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
open up you local host and port
```






## MLflow

- [Documentation](https://mlflow.org/docs/latest/index.html)

- [MLflow tutorial](https://youtu.be/qdcHHrsXA48?si=bD5vDS60akNphkem)

##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)

MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/Kidney-Disease-Classification-MLflow-DVC.mlflow \
MLFLOW_TRACKING_USERNAME=en****** \
MLFLOW_TRACKING_PASSWORD=******** \
python script.py

Run this to export as env variables:

```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/Kidney-Disease-Classification-MLflow-DVC.mlflow

export MLFLOW_TRACKING_USERNAME=en**** 

export MLFLOW_TRACKING_PASSWORD=*****

```


### DVC cmd

1. dvc init
2. dvc repro
3. dvc dag


## About MLflow & DVC

MLflow

 - Its Production Grade
 - Trace all of your expriements
 - Logging & taging your model


DVC 

 - Its very lite weight for POC only
 - lite weight expriements tracker
 - It can perform Orchestration (Creating Pipelines)



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

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

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/chicken

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = us-east-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

    ECR_REPOSITORY_NAME = simple-app


