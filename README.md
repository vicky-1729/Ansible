

# 🔄 Ansible Automation Projects

A comprehensive collection of Ansible playbooks, roles, and automation examples for infrastructure management and application deployment.

## 📂 Repository Structure

This repository is organized into the following sections:


### [Ansible Practice](./ansible-practice/)

A collection of Ansible playbooks and examples for learning and practicing Ansible concepts:

- **Basic Playbooks**: [01-playbook.yml](./ansible-practice/01-playbook.yml), [02-pining_server.yml](./ansible-practice/02-pining_server.yml)
- **Service Installation**: [03.nginx_installtion.yml](./ansible-practice/03.nginx_installtion.yml), [05-nginx.yml](./ansible-practice/05-nginx.yml)
- **Variables**: 
  - [07-play_varables.yml](./ansible-practice/07-play_varables.yml) - Playbook-level variables
  - [08-task_varables.yml](./ansible-practice/08-task_varables.yml) - Task-level variables
  - [09-varables_prompt.yml](./ansible-practice/09-varables_prompt.yml) - User input variables
  - [10-varables_inventroy.yml](./ansible-practice/10-varables_inventroy.yml) - Inventory variables
  - [11-varables_args.yml](./ansible-practice/11-varables_args.yml) - Command-line arguments
  - [12-file_varables.yml](./ansible-practice/12-file_varables.yml) - External variable files
- **Ansible Facts**: [13-ansbile_facts.yml](./ansible-practice/13-ansbile_facts.yml)
- **Control Flow**: 
  - [14-conidtions.yml](./ansible-practice/14-conidtions.yml) - Conditional execution
  - [15-loops.yml](./ansible-practice/15-loops.yml) - Iteration and loops
- **Functions**: [16-functions.yml](./ansible-practice/16-functions.yml)
- **Documentation**: 
  - [Collections_and_Plugins.md](./ansible-practice/Collections_and_Plugins.md) - Information on extending Ansible

### [RoboShop Ansible Automation](./roboshop-ansible-automation/)

An Ansible-based automation project for deploying the RoboShop e-commerce application using playbooks:

- **Frontend Service**: [frontend.yml](./roboshop-ansible-automation/frontend.yml) - Web UI configuration
- **Catalogue Service**: [catalogue.yml](./roboshop-ansible-automation/catalogue.yml) - Product catalog management
- **User Service**: [user.yml](./roboshop-ansible-automation/user.yml) - User authentication and management
- **Cart Service**: [cart.yml](./roboshop-ansible-automation/cart.yml) - Shopping cart operations
- **Shipping Service**: [shipping.yml](./roboshop-ansible-automation/shipping.yml) - Shipping logistics
- **Payment Service**: [payment.yml](./roboshop-ansible-automation/payment.yml) - Payment processing
- **Database Components**:
  - [mongodb.yml](./roboshop-ansible-automation/mongodb.yml) - NoSQL database
  - [mysql.yml](./roboshop-ansible-automation/mysql.yml) - Relational database
  - [redis.yml](./roboshop-ansible-automation/redis.yml) - In-memory caching
- **Message Queue**:
  - [rabbitmq.yml](./roboshop-ansible-automation/rabbitmq.yml) - Message broker
- **Configuration Templates**: 
  - [repo_config/](./roboshop-ansible-automation/repo_config/) - Repository configurations
  - [service/](./roboshop-ansible-automation/service/) - Service definitions
- **Inventory**: [roboshop.ini](./roboshop-ansible-automation/roboshop.ini) - Host inventory file
- **Documentation**:
  - [ansible_module.md](./roboshop-ansible-automation/ansible_module.md) - Module documentation
  - [Troubleshooting_Steps.md](./roboshop-ansible-automation/Troubleshooting_Steps.md) - Common issues and solutions

### [RoboShop Ansible Roles](./roboshop-automation-ansible-roles/)

An enhanced version of RoboShop automation using Ansible roles for better modularity and reusability:

- **Main Playbook**: [main.yml](./roboshop-automation-ansible-roles/main.yml) - Orchestrates all roles
- **Roles**:
  - [common/](./roboshop-automation-ansible-roles/roles/common/) - Shared tasks and handlers
  - [frontend/](./roboshop-automation-ansible-roles/roles/frontend/) - Web UI deployment
  - [catalogue/](./roboshop-automation-ansible-roles/roles/catalogue/) - Product catalog service
  - [user/](./roboshop-automation-ansible-roles/roles/user/) - User management service
  - [cart/](./roboshop-automation-ansible-roles/roles/cart/) - Shopping cart service
  - [shipping/](./roboshop-automation-ansible-roles/roles/shipping/) - Shipping service
  - [payment/](./roboshop-automation-ansible-roles/roles/payment/) - Payment service
  - [mongodb/](./roboshop-automation-ansible-roles/roles/mongodb/) - MongoDB database
  - [mysql/](./roboshop-automation-ansible-roles/roles/mysql/) - MySQL database
  - [redis/](./roboshop-automation-ansible-roles/roles/redis/) - Redis cache
  - [rabbitmq/](./roboshop-automation-ansible-roles/roles/rabbitmq/) - RabbitMQ message broker

## 🚀 Getting Started

### Prerequisites

- Ansible (version 2.9 or higher)
- SSH access to target servers
- Python 3.x on managed nodes
- Proper inventory configuration

### Running Practice Playbooks

```bash
# Navigate to ansible-practice directory
cd ansible-practice

# Run a specific playbook
ansible-playbook -i vs.ini 01-playbook.yml

# Run a playbook with variables
ansible-playbook -i vs.ini 11-varables_args.yml -e "variable_name=value"
```

### Deploying RoboShop with Playbooks

```bash
# Navigate to roboshop-ansible-automation directory
cd roboshop-ansible-automation

# Deploy all components
./roboshop_server.sh

# Or deploy individual components
ansible-playbook -i roboshop.ini frontend.yml
ansible-playbook -i roboshop.ini catalogue.yml
# etc.
```

### Deploying RoboShop with Roles

```bash
# Navigate to roboshop-automation-ansible-roles directory
cd roboshop-automation-ansible-roles

# Deploy all components using roles
ansible-playbook -i roboshop.ini main.yml

# Deploy specific role
ansible-playbook -i roboshop.ini main.yml --tags "frontend"
```

## 📝 Key Concepts Covered

- **Ansible Playbooks**: YAML-based configuration files for defining automation tasks
- **Roles**: Reusable, modular units of automation logic
- **Variables**: Different methods for using and defining variables
- **Templates**: Dynamic configuration file generation with Jinja2
- **Handlers**: Triggered actions based on task changes
- **Conditionals**: Conditional execution of tasks
- **Loops**: Iteration through lists and dictionaries
- **Inventory Management**: Organizing target hosts and group variables
- **Facts**: Gathering and using system information
- **Tags**: Selective execution of tasks and roles

## 🔍 Project Highlights

- **Progressive Learning Path**: From basic playbooks to advanced role-based architecture
- **Real-World Application**: Complete e-commerce platform deployment
- **Best Practices**: Follows Ansible recommended patterns and practices
- **Modular Design**: Components can be deployed independently or together
- **Idempotent Execution**: Safe to run multiple times
- **Comprehensive Documentation**: Detailed notes and troubleshooting guides

## 📅 Last Updated

September 7, 2025
