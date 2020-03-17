# Deploy-Docker-Container-on-AWS

## Prerequisite 

-Install Docker
-Install AWS CLI

## Step 1: 

1. Create a repository on AWS ECR
Command:  aws ecr create-repository --repository-name docker-demo

2. Once AWS CLI, run commands:
aws ecr get-login --no-include-email --region us-east-1
Or 
aws ecr get-login --no-include-email --region us-east-1 | sh  to to authenticate fully.


3. Tag your image with the Amazon ECR registry:
docker tag dockerdemo aws_account_id.dkr.ecr.region.amazonaws.com/docker-demo

4. Push the image using the docker push command:
docker push aws_account_id.dkr.ecr.region.amazonaws.com/docker-demo


