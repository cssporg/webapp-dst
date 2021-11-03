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

# Destination cluster  (us-west-2 region)

# Step 1:Build Custom AMI with Packer
https://github.com/cssporg/packer



# Step 3: Provisioning infrastructure with Terraform
https://github.com/cssporg/terraform

# Step 4: Installing and configuring Web server using Ansible
https://github.com/cssporg/ansible

# Step 5: Result
http://PUBLICIP:80



# Step 3:  login to lb1 instance

login to lb1 instance 

eval `ssh-agent`

ssh-add -k .pem

ssh -A centos@publicip




 sudo systemctl start docker && sudo groupadd docker && sudo usermod -aG docker $USER && sudo chmod 777 /var/run/docker.sock

$git clone https://github.com/csporg/webapp.git

$cd webapp/src/haproxy

$vi haproxy.cnf(line numbers 77 and 80)

$ docker build -t my-haproxy .

$ docker run -d --name my-running-haproxy -p 80:80 my-haproxy


# Step 4 :  login to lb1 instance
login to app1 instance

sudo yum install docker -y && sudo systemctl start docker && sudo groupadd docker && sudo usermod -aG docker $USER && sudo chmod 777 /var/run/docker.sock

$git clone https://github.com/csporg/webapp.git

$cd webapp/src/flask

vi index.py

$docker image build -t flask . or $docker image build -t flask --network host .

