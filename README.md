# Terraform AWS EKS

Production-ready Terraform modules for AWS EKS clusters.

## Features
- Multi-AZ deployment
- Managed node groups
- IRSA (IAM Roles for Service Accounts)
- Cluster autoscaler integration
- VPC with public/private subnets

## Usage
```hcl
module "eks" {
  source = "./modules/eks"
  
  cluster_name = "production"
  vpc_id       = module.vpc.vpc_id
  node_count   = 3
}
```

## License
Apache 2.0
