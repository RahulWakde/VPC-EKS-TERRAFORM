# VPC-EKS-TERRAFORM-NGINX
# Deploying an Amazon EKS Cluster Using Terraform

This project uses Terraform to provision an Amazon EKS cluster on AWS following Infrastructure as Code best practices, with a sample NGINX workload to validate the setup.
# Architecture Overview

The infrastructure created by this project includes:

- A VPC spanning multiple Availability Zones
- Public subnets for load balancers
- Private subnets for worker nodes
- EKS control plane managed by AWS
- EC2 worker nodes managed via EKS Node Groups
- 
#Prerequisites

- Terraform
- AWS CLI v2
- kubectl
- 
#Folder Breakdown

- ConfigurationFiles/
 Kubernetes manifests for deploying workloads (Deployment & Service).

- eks-module/
 Reusable Terraform module that creates the VPC, networking, IAM roles, EKS cluster, and node groups.

- Root files (main.tf, provider.tf, variables.tf)
 Used to configure providers, define variables, and call the EKS module.
