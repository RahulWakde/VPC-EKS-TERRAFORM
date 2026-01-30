# VPC-EKS-TERRAFORM
3EKS Cluster on AWS Using Terraform

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
