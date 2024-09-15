# End-to-end-Machine-Learning-Project-with-MLflow
 
  
## Workflows

1. Update config.yaml 
2. Update schema.yaml
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the app.py



# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/Arsalan-Azhar-AI/End-to-end-Machine-Learning-project-with-mlflow
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n mlproj python=3.8 -y
```

```bash
conda activate mlproj
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

[Documentation](https://mlflow.org/docs/latest/index.html)


##### cmd
- mlflow ui

### dagshub
[dagshub](https://dagshub.com/)
https://dagshub.com/arsalanazhar2003/End-to-end-Machine-Learning-project-with-mlflow.mlflow

Run this to export as env variables:

```bash

export https://dagshub.com/arsalanazhar2003/

export MLFLOW_TRACKING_USERNAME=entbappy 

export MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0

```
powershell 
'''
$env:MLFLOW_TRACKING_URI= "https://dagshub.com/arsalanazhar2003/End-to-end-Machine-Learning-project-with-mlflow.mlflow"

$env:MLFLOW_TRACKING_USERNAME="arsalanazhar2003"
$env:MLFLOW_TRACKING_PASSWORD="ddbdda8eff3c518a6b060fc3d7a9cd36bc8c292d"


'''
for ipynb
'''

os.environ["MLFLOW_TRACKING_URI"]="https://dagshub.com/arsalanazhar2003/End-to-end-Machine-Learning-project-with-mlflow.mlflow"
os.environ["MLFLOW_TRACKING_USERNAME"]="arsalanazhar2003"
os.environ["MLFLOW_TRACKING_PASSWORD"]= "ddbdda8eff3c518a6b060fc3d7a9cd36bc8c292d"


'''



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment ->"Search iam -> user -> create user -> set below mention Policy -> then it successfully created, now view it, then click some thing like security and access key. -> creat token. it successfully created. may some step missed. "

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
    - Save the URI: 116981778199.dkr.ecr.ap-southeast-2.amazonaws.com/mlproj ->"Its a simple just create repo and paste the url here."

	
## 4. Create EC2 machine (Ubuntu) ->"serach EC2 -> instance -> lanch instance -> give name -> select for ubuntu -> select instance type is t2.large because 8 Gib sufficient. -> create or write in key pair option. -> select the two options 'Allow HTTPS traffic from the internet' and 'Allow HTTP traffic from the internet'-> select 32 configure storage ->  click lanch instance. it will created. now view instance and make sure inatance state is running. so next is click on instance id and click on connect button. you will see the terminal and make the terminal clear. now run all the command one by one that mention in the next step called 5."

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




## About MLflow 
MLflow

 - Its Production Grade
 - Trace all of your expriements
 - Logging & tagging your model
'''
