# Infrastructure_2019

# Automating running GitLab on AWS with Terraform.

# Prerequisites.

OS = Centos7
Instance_type
S3 Bucket
Route53
AMI = image
Zone_id 
VPC_id
Region

Using provider AWS account and Terraform.
Need to create a bastion host so we can jump into our VPC and access other resources in public subnnet.
In ordre for Terraform to deploy you will need the resources in AWS account, you will need to set the AWS credentials for user with the proper permissions.
To start you'll need a VPC in which to create all your resources.
VPC wiil create across two availability zones: two private and public subnets,corrsponding NAT instances,with all route tables set up for you.
You need two new variables, your `key_name` and `ssh_public_key` is the name of an EC2 key pair to assign to instances.
Create a file `terraform.tfvars` to hold the values to your variables.
On the terraform directory in your terminal you can run `terreaform init`
On the terminal start running this commnads: 
`terraform init`
`terraform plan`
`terraform apply --var -file=gitlab.tfvars`
"YOU SHOULD ALWAYS INSPECT THE OUTPUT OF THE TERRAFORM BEFORE APPLYIN BY RUNNING THE COMMAND `terraform plan` "


