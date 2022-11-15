ECS-EC2LAUNCHCONFIG-WITHTERRAFORM

AIM:

.Provisioned some building blocks:

.a VPC with a public subnet as an isolated pool for our resources

.Internet Gateway to contact the outside world

.Security groups for RDS MySQL and for EC2s

.Auto-scaling group for ECS cluster with launch configuration

.RDS MySQL instance

.ECR container registry

.ECS cluster with task and service definition

This repo can be used to deploy an ECS cluster with Fargate launch type on Terraform.

Variable.tf

Using a variable.tf file makes it easy for this project to be reaused.
Changes can easily be made in the variable.tf. Thus, you can make changes such as CIDR values for VPC, Availability zones, Region, port app etc.
Customize to suit your requirements.

Prerequisites for this to work correctly:

An AWS account configured to your local envirionment. If you are using IAM User's credential, it should have permission to make changes/manage all resources using terraform. Terraform installed on your local machine Visual Code installedon you machine



Terraform Commands and Good practices

First Run 'terraform init' on terminal to initialize a working directory containing Terraform configuration files

use 'terraform fmt' to rewrite/ arrange the code to an Terraform standard

use 'terraform validate' make sure everything is valid

use 'terraform plan' will give tell you all the resources you are about to create

use 'terraform apply' to provision your resources

use 'terraform destroy' to destroy the resources created
