# Terraform AWS EKS Cluster

Production-ready Amazon EKS cluster provisioning with Terraform. Includes VPC, node groups, IAM roles, and cluster autoscaler configuration.

## Architecture
- **VPC**: Multi-AZ with public/private subnets
- **EKS**: Managed Kubernetes cluster with Fargate profiles
- **Node Groups**: Spot and on-demand EC2 instances
- **Autoscaler**: Cluster autoscaler + HPA integration

## Prerequisites
- Terraform >= 1.5
- AWS CLI configured
- kubectl

## Usage
```bash
terraform init
terraform plan -var-file="environments/prod.tfvars"
terraform apply -var-file="environments/prod.tfvars"
```

## Module Structure
- `modules/vpc/` - VPC and networking
- `modules/eks/` - EKS cluster and node groups
- `modules/iam/` - IAM roles and policies
