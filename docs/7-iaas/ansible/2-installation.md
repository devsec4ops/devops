#Initial Setup

## Ansible Isntallation 
### macOS

-   Install Homebrew: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
-   Install Ansible: `brew update && brew install ansible`

### Windows (WSL)

-   Enable WSL, install a Linux distro from Microsoft Store (e.g., Ubuntu).
-   Install Ansible: `sudo apt update && sudo apt install ansible`

### Linux

-   Debian/Ubuntu: `sudo apt update && sudo apt install ansible`
-   Red Hat/CentOS: `sudo yum install epel-release && sudo yum update && sudo yum install ansible`
-   Fedora: `sudo dnf install ansible`

## Install Boto3 and Botocore
Boto3 is the Amazon Web Services (AWS) SDK for Python. It's required for Ansible modules to interact with AWS.
`pip install boto3 botocore`
## Set up AWS Credentials
Create an IAM user in AWS with programmatic access.
Run aws configure and enter your AWS Access Key ID, Secret Access Key, default region, and output format.
## Create a Static Inventory File (e.g., hosts):
Add [local] and localhost ansible_connection=local to run tasks on your local machine.

