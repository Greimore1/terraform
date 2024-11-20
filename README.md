# Terraform AWS Web Server Deployment

## Project Overview
This project uses Terraform and GitHub Actions to automatically deploy a simple web server on AWS EC2, demonstrating infrastructure as code (IaC) and continuous deployment.

## Features
- Automatically creates an EC2 instance in the eu-west-2 region
- Sets up a security group allowing HTTP traffic
- Installs and configures Apache web server
- Displays a "Hello, World!" page
- Uses GitHub Actions for CI/CD workflow

## Prerequisites
- AWS Account
- GitHub Account
- Terraform installed locally (optional)

## Setup
1. Configure AWS credentials in GitHub repository secrets:
   - `AWS_ACCESS_KEY_ID`
   - `AWS_SECRET_ACCESS_KEY`

2. Ensure GitHub Actions workflow is enabled

## Workflow
- Pushes to `main` branch trigger automatic deployment
- Pull requests run `terraform plan` for preview

## Resources Created
- EC2 Instance (t2.micro)
- Security Group
- Default VPC

## Output
The public IP address of the deployed web server is output after successful deployment.

## Security Note
- Inbound HTTP traffic is allowed from any IP (0.0.0.0/0)
- Outbound traffic is unrestricted

## License
MIT License
