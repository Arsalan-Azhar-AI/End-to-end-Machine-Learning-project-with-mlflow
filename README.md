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
https://dagshub.com/enthapy/End-to-end-Machine-Learning-project-with-mlflow.mlflow

Run this to export as env variables:

```bash

export https://dagshub.com/email@gmail.com/

export MLFLOW_TRACKING_USERNAME=entbappy 

export MLFLOW_TRACKING_PASSWORD=6824692c47a369aa6f9eac5b10041d5c8edbcef0

```
powershell 
'''
$env:MLFLOW_TRACKING_URI= "###################################" -> "Replace your mlflow url"

$env:MLFLOW_TRACKING_USERNAME="#################" -> "Replace your email"
$env:MLFLOW_TRACKING_PASSWORD="##############" -> "Replace your password"


'''
for ipynb
'''

os.environ["MLFLOW_TRACKING_URI"]="###################################" -> "Replace your mlflow url"
os.environ["MLFLOW_TRACKING_USERNAME"]="#################" -> "Replace your email"
os.environ["MLFLOW_TRACKING_PASSWORD"]= "##############" -> "Replace your password"


'''



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment ->"Search iam -> user -> create user -> set below mention Policy -> then it successfully created, now view it, then click some thing like security credential. -> create token. it successfully created. may some step missed. "

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
    - Save the URI: 1566373416292.dkr.ecr.ap-south-1.amazonaws.com/sample-app ->"Its a simple just create repo and paste the url here."

	

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
    setting>actions>runner>new self hosted runner> choose os> then run command one by one ->"Go to github -> make copy of your github repo -> then follow these steps. 'setting>actions>runner>new self hosted runner> choose any os> then run command one by one' run these command one by one on command prompt that i access through aws instance. if any things it ask it present in the github sittings current page where all the commands are present "

# 7. Setup github secrets: -> "Go to github -> secrets and variables -> Actions -> New repositort secret -> paste the name and scret id that present to csv file that i download from aws. -> click Add secret button."

    AWS_ACCESS_KEY_ID=

    AWS_SECRET_ACCESS_KEY=

    AWS_REGION = p-south-1

    AWS_ECR_LOGIN_URI = demo>>  566373416292.dkr.ecr.ap-south-1.amazonaws.com


    ECR_REPOSITORY_NAME = simple-app

after setting step 7 make change the port of app.py. and push all the code on github. then go to github action. it start runing the workflow.

the final step is go to aws->ec2->instance->instance id->security->click on security group link -> then click on edit inbound rules button -> add port 8080 and 0.0.0.0/0 and save the rules.-> go to the ec2 instance id-> copy the public url and paste it in new tab like example 3.147.57.12:8080
 Congrajulations for completed end to end.

## About MLflow 
MLflow

 - Its Production Grade
 - Trace all of your expriements
 - Logging & tagging your model
'''


<<<<<< Deploy on Azure Plateform with github action using CICD >>>>>>>>

 #1 Login to Azure.
 
 #2 Serach container registry -> creat new registry -> create new resource group -> write Registry name -> press next and make all the remaining things by default and it will created.
   then in container registry click on button Go to Resource -> in setting click on access keys and enabled the  Admin user. -> Copy the Login server and password because it use later on.

#3 create or serach Web App -> Create Resource Group -> write Name in Instance Details -> Markdown Docker Container -> Select Region like Centrl US or etc -> next ->option will be Single Container -> Image Source will be Azure Container Registry -> select registry -> seclet image if image is not present follow the step mention in 6666 if present move next here. -> tag should be latest -> next,networking -> and remaining all the things is default and click next and its created.

#4 Go to deployment center and you see the cotainer registry and web app.-> click on your created container registry -> click on Container Registry:set up your app to pull the container image from a registry -> click on Continuous deployment On. -> click on Github action: Build deploy .... option -> select orgonization like you github account -> select github repositry name -> select branch like main -> and save this.-> go to github actions automatically deployment start and after deployment copy the url of your web and congragulations for completed all the thngs.  

#6666. open docker desktop-> then in your vs code terminal run these command.
  docker build -t testdockerkrish.azurecr.io/mltest:latest ->"make sure update these name to my own names. these are copy from azure registry."
  
  docker login testdockerkrish.azurecr.io->"make sure update these name to my own names. write user name and password that copy from azure container registry if ask."

  docker push testdockerkrish.azurecr.io/mltest:latest->"make sure update these name to my own names."

  "after these go to conainer registry -> repositry -> search for docker images -> click -> you find entire information about the docker image. "

finally go to resource group and delete the resources.

  
