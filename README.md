# Project Title
This project is intended to touch and feel containerized Web Application. 


# Destination cluster  (us-west-2 region)


# Step 3: Provisioning infrastructure with Terraform
https://github.com/cssporg/terraform

# Destination cluster

$git clone https://github.com/cssporg/infra_manager.git

$cd infra_manager

$vi config.json

mykeypair : ""

myamiid : ""


$ vi modules/computing/ec2/instances.tf

variable "wrpilwsn" {

type = "list"

default = [

"10.0.20.52,0",

"10.0.20.86,1"

]

}


#subnet_id = "${var.enable_user_defined_ips ? element(var.appsubnet, element(split(":", element(var.appserver_pa_ips, count.index)),1)) : element(var.appsubnet, count.index)}"

#private_ip = "${var.enable_user_defined_ips ? element(split(":", element(var.appserver_pa_ips, count.index),0)) : ""}"

subnet_id = "${element(var.appsubnet, element(split(",", element(var.wrpilwsn, count.index)), 1))}"

private_ip = "${element(split(",", element(var.wrpilwsn, count.index)), 0)}"


$terraform init .

$terraform validate -var-file=config.json

$terraform apply -var-file=config.json



# After disaster

vi config.json

"rds_mysql_db" : {
  "recover" : "true",
  "snapshot_names" : "rds-mysql-db-snp"
}



# Step 4: Installing and configuring Web server using Ansible
https://github.com/cssporg/ansible

# Step 5: Result
http://PUBLICIP:80
