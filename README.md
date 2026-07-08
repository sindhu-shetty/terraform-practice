# Terraform AWS Infrastructure

Terraform project provisioning complete AWS infrastructure from scratch.

## What This Project Builds

- **VPC** — custom virtual private cloud (10.0.0.0/16)
- **Public Subnet** — in ap-south-1a availability zone
- **Internet Gateway** — connects VPC to internet
- **Route Table** — routes internet traffic via gateway
- **Security Group** — allows SSH (22) and HTTP (80)
- **EC2 Instance** — Ubuntu 22.04, t3.micro (free tier)
- **Output** — displays public IP after creation

## Usage

```bash
# Initialize
terraform init

# Preview changes
terraform plan

# Create infrastructure
terraform apply

# Connect to EC2
ssh -i ~/.ssh/sindhu-key.pem ubuntu@<public_ip>

# Destroy everything
terraform destroy
```

## Architecture
