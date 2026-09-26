# AWS Infrastructure & Ansible Automation Project

## Project Overview

This project demonstrates how I used Terraform and Ansible together to provision and automate Linux servers on AWS.

Terraform is used to provision the AWS EC2 infrastructure, while Ansible is used to configure, patch, and manage the servers automatically.

The environment is divided into Production and Test servers to demonstrate infrastructure provisioning and configuration management across multiple environments.

## Architecture

- AWS Cloud
- 10 EC2 instances
  - 5 Production servers
  - 5 Test servers
- Terraform for infrastructure provisioning
- Ansible for server configuration and automation
- Amazon Linux
- Docker
- Nginx

## Terraform

Terraform is used to provision the AWS infrastructure, including:

- EC2 instances
- Production and Test environments
- Security groups
- SSH access configuration
- Infrastructure outputs such as server public IP addresses

## Ansible

After Terraform provisions the servers, Ansible is used to configure and manage them.

The Ansible automation includes:

- Managing Production and Test server groups through inventory
- Installing required packages
- Starting and enabling Docker and Nginx services
- Creating Linux users
- Creating Linux groups
- Creating application and operational directories
- Managing directory permissions and ownership
- Updating and patching installed packages
- Deploying Nginx configuration
- Using handlers to restart Nginx when configuration changes
- Verifying Nginx after configuration
- Using variables and loops to make the playbooks reusable
- Demonstrating idempotent configuration management

## Ansible Concepts Practiced

This project demonstrates practical use of:

- Inventory
- Playbooks
- Variables
- Loops
- Package module
- Service module
- User and Group modules
- File module
- Copy module
- Command module
- Handlers
- Privilege escalation (`become`)
- Idempotency

## Project Structure

    ansible-automation-project/
    ├── Terraform/
    │   └── Terraform configuration files
    ├── production_practice.yml
    ├── test_setup.yml
    ├── variables.yml
    ├── nginx.conf
    └── README.md

## Workflow

    Terraform
        |
        v
    AWS EC2 Infrastructure
        |
        v
    Ansible Inventory
        |
        v
    Ansible Playbooks
        |
        +--> Install Packages
        +--> Configure Services
        +--> Create Users & Groups
        +--> Configure Permissions
        +--> Patch Servers
        +--> Deploy Nginx Configuration
        |
        v
    Production & Test Servers

## Skills Demonstrated

AWS | Terraform | Ansible | Linux | Docker | Nginx | Infrastructure as Code | Configuration Management | Server Automation
