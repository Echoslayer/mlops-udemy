### MLFLOW On AWS

## MLflow on AWS Setup:

- [主控台首頁 | 控制台首頁 | ap-southeast-2](https://ap-southeast-2.console.aws.amazon.com/console/home?region=ap-southeast-2)
- [AWS CLI](https://aws.amazon.com/tw/cli/)
- [安裝或更新至最新版本的 AWS CLI - AWS Command Line Interface](https://docs.aws.amazon.com/zh_tw/cli/latest/userguide/getting-started-install.html)
- [雲端物件儲存 – Amazon S3 – Amazon Web Services](https://aws.amazon.com/tw/s3/)

1. Login to AWS console.
2. Create IAM user with AdministratorAccess
3. Export the credentials in your AWS CLI by running "aws configure"
4. Create a s3 bucket
5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following command on EC2 machine
```bash
sudo apt update

sudo apt install python3-pip

sudo apt install pipenv

sudo apt install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflowtracking1

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=http://ec2-54-158-152-207.compute-1.amazonaws.com:5000/