# DeepScan-Automated-Chest-Cancer-Detection-Using-MLflow-and-DVC



###Workflows

Update config.yaml, run the following command to start a new experiment:
Update secrets.yaml [Optional], run the following command to start a new experiment:
Update params.yaml, run the following command to start a new experiment:
Update the entity, run the following command to start a new experiment:
Update the configuration manager in src config, run the following command to start a new experiment:
Update the components, run the following command to start a new experiment:
Update the pipeline, run the following command to start a new experiment:
Update the main.py, run the following command to start a new experiment:
Update the dvc.yaml, run the following command to start a new experiment:


# ###dagshub
[dagshub](https://dagshub.com/)


MLFLOW_TRACKING_URI=https://dagshub.com/pawanchinnu17/DeepScan-Automated-Chest-Cancer-Detection-Using-MLflow-and-DVC.mlflow \
MLFLOW_TRACKING_USERNAME=pawanchinnu17 \
MLFLOW_TRACKING_PASSWORD=afa64adc979875924b96b19bd10958adf02a2ad1 \
python script.py

to run this  project locally you need to install mlflow and other dependencies using pip install -r requirements.txt


# export MLFLOW_TRACKING_URI=https://dagshub.com/pawanchinnu17/DeepScan-Automated-Chest-Cancer-Detection-Using-MLflow-and-DVC.mlflow 

# export MLFLOW_TRACKING_USERNAME=pawanchinnu17

# export MLFLOW_TRACKING_PASSWORD=afa64adc979875924b96b19bd10958adf02a2ad1

DVC cmd
dvc init
dvc repro
dvc dag
About MLflow & DVC
MLflow

Its Production Grade
Trace all of your expriements
Logging & taging your model
DVC

Its very lite weight for POC only
lite weight expriements tracker
It can perform Orchestration (Creating Pipelines)
AWS-CICD-Deployment-with-Github-Actions
1. Login to AWS console.
2. Create IAM user for deployment
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
3. Create ECR repo to store/save docker image
- Save the URI: 566373416292.dkr.ecr.us-east-1.amazonaws.com/chicken
4. Create EC2 machine (Ubuntu)
5. Open EC2 and Install docker in EC2 Machine:
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
6. Configure EC2 as self-hosted runner:
setting>actions>runner>new self hosted runner> choose os> then run command one by one
7. Setup github secrets:
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = us-east-1

AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com

ECR_REPOSITORY_NAME = simple-app