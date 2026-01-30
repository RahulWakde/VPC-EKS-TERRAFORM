# VPC-EKS-TERRAFORM-NGNIX
EKS Cluster on AWS Using Terraform

In this project, I’ve built an Amazon EKS cluster using Terraform, following infrastructure-as-code principles and AWS best practices.
The goal of this setup is to create a reproducible, clean, and production-ready Kubernetes environment without relying on manual AWS Console steps.
# Architecture Overview

This Terraform configuration provisions:

- A custom VPC
- Public and private subnets
- Internet Gateway
- NAT Gateway
- EKS control plane
- Managed node groups
- Required IAM roles and security groups

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
