# Terraform AWS EKS

Production-ready Terraform modules for AWS EKS clusters.

## Features
- Multi-AZ deployment
- Managed node groups
- IRSA (IAM Roles for Service Accounts)
- Cluster autoscaler integration

## Usage
```hcl
module "eks" {
  source = "./modules/eks"
  cluster_name = "production"
}
```

## License
Apache 2.0
