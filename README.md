# Terraform AWS EKS Cluster

Production-ready Amazon EKS cluster provisioning with Terraform. Includes VPC, managed node groups, IAM roles, and cluster autoscaler configuration.

## Architecture
- **VPC**: Multi-AZ with public/private subnets and NAT Gateway
- **EKS**: Managed Kubernetes cluster with KMS encryption
- **Node Groups**: Spot + on-demand EC2 instances with auto-scaling
- **Logging**: CloudWatch audit, controller, and scheduler logs

## Prerequisites
- Terraform >= 1.5.0
- AWS CLI configured with appropriate credentials
- kubectl >= 1.28

## Usage
```bash
terraform init
terraform plan -var-file="environments/prod.tfvars"
terraform apply -var-file="environments/prod.tfvars"
```

## Module Structure
- `modules/vpc/` - VPC, subnets, NAT Gateway, route tables
- `modules/eks/` - EKS cluster, node groups, security groups
- `modules/iam/` - IAM roles for cluster and node group
