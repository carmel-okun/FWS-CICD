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

## installing docker
### source: https://docs.docker.com/engine/install/ubuntu/

for pkg in docker.io docker-doc docker-compose docker-compose-v2 podman-docker containerd runc; do sudo apt-get remove $pkg; done

sudo apt-get update

sudo apt-get install ca-certificates curl

sudo install -m 0755 -d /etc/apt/keyrings

sudo curl -fsSL \https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc

sudo chmod a+r /etc/apt/keyrings/docker.asc

echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose docker-compose-plugin

sudo groupadd docker

sudo usermod -aG docker $USER

newgrp docker
