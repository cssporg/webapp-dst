# Project Title
This project is intended to touch and feel containerized Web Application. 

# Pre-Requisites

Launch ec2 instance to run terraform with name sandbox

Login to sandbox instance

$sudo yum install git -y 

$git clone https://github.com/cssporg/webapp.git

$cd DevOps

$sh sandbox.sh

$source export.sh

# Source cluster  (us-east-1 region)

# Step 1:Build Custom AMI with Packer
https://github.com/cssporg/packer



# Step 3: Provisioning infrastructure with Terraform
https://github.com/cssporg/terraform

# Step 4: Installing and configuring Web server using Ansible
https://github.com/cssporg/ansible

# Step 5: Result
http://PUBLICIP:80



# Destination cluster  (us-west-2 region)

# Step 1:Build Custom AMI with Packer
https://github.com/cssporg/packer



# Step 3: Provisioning infrastructure with Terraform
https://github.com/cssporg/terraform

# Step 4: Installing and configuring Web server using Ansible
https://github.com/cssporg/ansible

# Step 5: Result
http://PUBLICIP:80
