pipeline {
  agent any

  environment {
    AWS_REGION = "us-west-2"
    AWS_CREDENTIALS = credentials('aws-cred')
  }

  stages {
    stage('Checkout') {
      steps {
        git url: 'https://github.com/RahulWakde/VPC-EKS-TERRAFORM.git', branch: 'main'
      }
    }

    stage('Terraform Init') {
      steps {
        dir('eks-module') {
          sh 'terraform init'
        }
      }
    }

    stage('Terraform Apply') {
      steps {
        dir('eks-module') {
          sh 'terraform apply -auto-approve'
        }
      }
    }

    stage('Deploy Nginx') {
      steps {
        dir('ConfigurationFiles') {
          sh 'kubectl apply -f deployment.yaml'
          sh 'kubectl apply -f service.yaml'
        }
      }
    }
  }
}

