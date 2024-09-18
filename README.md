# FWS-CICD

## installing Ansible
### source: https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
### source: https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html#installing-ansible-on-ubuntu

sudo apt update

sudo apt install software-properties-common

sudo add-apt-repository --yes --update ppa:ansible/ansible

sudo apt install ansible

## installing boto3 & botocore

sudo apt install python3-pip

sudo apt install python3-boto3

sudo apt install python3-botocore

## installing aws ansible collection

ansible-galaxy collection install amazon.aws

## installing awscli

### source: [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)

[](https://github.com/carmel-okun/platform-engineering/tree/dev#source-httpsdocsawsamazoncomclilatestuserguidegetting-started-installhtml)

curl "[https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip](https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip)" -o "awscliv2.zip"

sudo apt install unzip

unzip awscliv2.zip

sudo ./aws/install

## configure aws credentials

aws configure

## IAM role

give control node instance AmazonEC2FullAccess iam role

