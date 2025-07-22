# WordPress on EC2 via Ansible - Professional Deployment Solution

[![Ansible](https://img.shields.io/badge/ansible-2.10%2B-red.svg)](https://www.ansible.com/)
[![Terraform](https://img.shields.io/badge/terraform-1.5%2B-blue.svg)](https://www.terraform.io/)
[![WordPress](https://img.shields.io/badge/wordpress-6.0%2B-blue.svg)](https://wordpress.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![EC2](https://img.shields.io/badge/AWS-EC2-orange.svg)](https://aws.amazon.com/ec2/)

## Project Overview
This repository provides an automated, production-grade solution for deploying WordPress with WooCommerce capabilities on AWS EC2 instances. The infrastructure is provisioned using Terraform/Ansible with a focus on:

- **Infrastructure as Code**: Fully automated provisioning and configuration
- **Security First**: Hardened server configuration from ground up
- **DevOps Best Practices**: Idempotent playbooks, role-based organization
- **Cost Optimization**: Efficient resource utilization on AWS
- **Client-Ready**: Pre-configured with demo content for immediate showcase

## Key Features
### Infrastructure Automation
-  AWS EC2 instance provisioning
-  VPC security group configuration
-  Route53 DNS integration
-  Automatic SSH key management
-  Multi-environment support

### Application Stack
- 🚀 Latest WordPress with WooCommerce
- 🔒 Secure LEMP stack (Nginx, PHP 8.1, MySQL)
- 📦 WP-CLI integration for management
- 🎭 20+ sample products with categories
- 🖼️ Demo content (pages, posts, media)

### Security Hardening
- 🔥 UFW firewall (SSH/HTTP/HTTPS only)
- 👤 Non-root user with sudo privileges
- 🔑 SSH key authentication only
- 🛡️ Fail2ban intrusion prevention
- 🔄 Automatic security updates
- 📈 SSL A+ rating configuration

### DevOps Best Practices
- ♻️ Idempotent playbooks (safe to rerun)
- 🧩 Modular role-based architecture
- 🔍 Detailed logging and output
- ⏱️ Quick deployment (~8-10 minutes)
- 🗑️ Clean resource teardown

## Architecture
```mermaid
graph TD
    A[Local Machine] -->|Ansible| B[AWS EC2]
    B --> C[Security Group]
    B --> D[Ubuntu 22.04 LTS]
    D --> E[Nginx]
    D --> F[PHP-FPM 8.1]
    D --> G[MySQL 8.0]
    E --> H[WordPress]
    F --> H
    G --> H
    H --> I[WooCommerce]
    H --> J[Demo Content]
    D --> K[Certbot SSL]
    D --> L[UFW Firewall]
    D --> M[Fail2Ban]
    D --> N[Non-root User]
```
