# Week3 Infrastructure Provisioning - Terraform (Days 20–26)

## Goal

Automate infrastructure creation using Terraform so you don’t rely on manual clicks.

## Time Commitment

1.5–2 hours per day, 5–7 days.

## What To Expect

By the end of Week 3, you should:
- Understand Terraform fundamentals
- Be able to write a small Terraform configuration to create a VM and maybe a bucket
- Know what state is and why it matters (common interview question)

ALSO You don’t need to know every Terraform feature.

## Step-by-Step

1. Learn Terraform basics
    
    Official tutorials:
    https://developer.hashicorp.com/terraform/tutorials/aws-get-started
    https://github.com/hashicorp/learn-terraform-provision-ec2-instance
    
    - Concepts to : provider, resource, variable, output, state
    - Commands: init, plan, apply, destroy.

2. Create your first configuration

  - Choose AWS or your main cloud
  - Use the “provision EC2” example as reference:
  https://github.com/hashicorp/learn-terraform-provision-ec2-instance
  
  - Write your own main.tf that creates:
  - VPC (optional for first step)
  - EC2/VM instance
  - A security group.

3. Use variables and outputs
  
  - Add variables.tf for region, instance typ
  - Add outputs.tf for instance ID, public IP.

4. Understand state
  Terraform state:
  https://developer.hashicorp.com/terraform/language/state
  
  - See terraform.tfstate file
  - Run apply, change something, then apply again
  - See how Terraform reconciles changes.

5. Clean up
  - Use terraform destroy
  - Confirm resources are removed from the console.

## Checklist
  - You can explain provider, resource, variable, and state
  - You have created at least one VM using Terraform
  - You have used init, plan, apply, and destroy
  - You understand that Terraform tracks infra in state


## Practice Resources
  Free Labs: 
  https://kodekloud.com/free-labs/terraform
  https://collabnix.github.io/terraform/

## Additional Resources for reference
  https://developer.hashicorp.com/terraform/tutorials/aws-get-started
  https://github.com/hashicorp/learn-terraform-provision-ec2-instance
  https://developer.hashicorp.com/terraform/language/state

## What Won’t Work

  Copying Terraform templates blindly.
  Type your own code and understand how each block connects.
