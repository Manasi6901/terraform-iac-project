🚀 Infrastructure as Code with Terraform

This project demonstrates how to provision AWS infrastructure using Terraform. It follows the Infrastructure as Code (IaC) approach to build, manage, and destroy cloud resources efficiently.

📌 Project Overview

Using Terraform, this project provisions:

✅ VPC (Virtual Private Cloud)

✅ Public Subnet

✅ Internet Gateway & Route Tables

✅ Security Group (allows SSH & HTTP)

✅ EC2 Instance (Amazon Linux 2)

The infrastructure is fully automated and reusable.

📂 Project Structure
terraform-iac-project/
│── main.tf          # Main Terraform configuration
│── variables.tf     # Input variables
│── outputs.tf       # Output values
│── provider.tf      # Provider configuration

⚙️ Prerequisites

AWS Account

Terraform installed → Install Guide

AWS CLI configured (aws configure)

IAM user with programmatic access

🚀 How to Run
1️⃣ Clone the Repository
git clone https://github.com/your-username/terraform-iac-project.git
cd terraform-iac-project

2️⃣ Initialize Terraform
terraform init

3️⃣ Preview Resources
terraform plan

4️⃣ Apply Configuration
terraform apply -auto-approve


Terraform will create:

A VPC, subnet, and route table

Internet Gateway

Security Group (SSH + HTTP access)

EC2 instance with a public IP

5️⃣ Access EC2 Instance
ssh ec2-user@<public_ip>


⚠️ Replace <public_ip> with the output shown after apply.

🧹 Cleanup

To destroy all resources and avoid costs:

terraform destroy -auto-approve

📜 Outputs

After deployment, Terraform provides:

ec2_public_ip → Public IP of EC2 instance

ec2_public_dns → Public DNS of EC2 instance

📌 Next Steps

Extend this project into a multi-tier architecture (EC2 + RDS + Load Balancer).

Add Terraform modules for reusability.

Integrate with CI/CD pipelines for automated deployments.

🛠️ Tools & Technologies

Terraform

AWS (EC2, VPC, Subnets, Security Groups)

Infrastructure as Code (IaC)
